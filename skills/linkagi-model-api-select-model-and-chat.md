---
name: Select a live model and call LinkAGI Chat Completions
description: Read the live LinkAGI price/model table, pick a model the token's group can actually address, then send an OpenAI-compatible Chat Completions request without wasting prepaid balance.
api: openapi/linkagi-model-api-openapi.json
operations:
  - getPublicPricing
  - listModels
  - createChatCompletion
generated: '2026-08-09'
method: generated
source: openapi/linkagi-model-api-openapi.json + https://docs.linktoagi.com/
---

# Select a live model and call LinkAGI Chat Completions

LinkAGI is a relay (中转站), not a model vendor. Model ids, prices and pools change without notice,
and a key only sees the models enabled for its **group** (号池). Never hardcode a model id.

## 1. Read the live catalogue first — `getPublicPricing`

`GET https://api.linktoagi.com/api/pricing` — unauthenticated, no balance spent.

Use the response to decide:

- `data[]` — one entry per model: `model_name`, `model_ratio`, `completion_ratio`, `cache_ratio`,
  `enable_groups[]`, `supported_endpoint_types[]`.
- `usable_group` / `group_ratio` — the groups that exist and their multipliers.
- `supported_endpoint` — which path serves which protocol.
- `pricing_version` — record it alongside any price you quote. It is a hash; when it changes, your price is stale.

Pick a model whose `supported_endpoint_types` contains `openai` and whose `enable_groups` contains
the group your token belongs to.

## 2. Confirm what the token can see — `listModels`

`GET https://api.linktoagi.com/v1/models` with `Authorization: Bearer <key>`.

- `401` means the key, the group, or the balance is wrong — **not** the model. See
  `errors/linkagi-model-api-problem-types.yml`.
- The provider states an authenticated model listing has not been re-verified in its latest evidence set,
  so treat step 1 as authoritative and this step as a cross-check.

## 3. Send the call — `createChatCompletion`

`POST https://api.linktoagi.com/v1/chat/completions` with `Authorization: Bearer <key>` and
`content-type: application/json`.

```json
{
  "model": "<copy from step 1>",
  "messages": [{"role": "user", "content": "Reply with: LinkAGI API ok"}],
  "stream": false,
  "max_tokens": 32
}
```

`messages[].role` is one of `system`, `developer`, `user`, `assistant`, `tool`.

## Rules

- **This call is billable.** It draws on a prepaid CNY balance. Start with `max_tokens: 32` on a new model.
- **There is no idempotency key.** A retry is a second billable call. After a `504`, check the console usage
  log before retrying.
- **429 is ambiguous.** It can be your rate, your concurrency, your balance, the pool, or the upstream
  vendor. Back off exponentially, cap concurrency, and read the call log to find the layer.
- **Capture `x-oneapi-request-id`** from every response. Support cannot help without it; it is also appended
  to `error.message`.
- **Errors are not RFC 9457.** Expect `{"error":{"code":"","message":"...","type":"new_api_error"}}`.
- **Streaming is unverified** by the provider. `stream: true` is accepted by the schema but not part of the
  published evidence set.
