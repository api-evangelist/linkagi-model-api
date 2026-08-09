---
name: Point Codex at LinkAGI and call the Responses route
description: Configure a Responses-protocol client (Codex CLI) against the LinkAGI relay and send a createResponse call, avoiding the two failures that dominate this path — 404 Invalid URL from a mis-set base URL and 401 Invalid token from the wrong group.
api: openapi/linkagi-model-api-openapi.json
operations:
  - getPublicPricing
  - createResponse
generated: '2026-08-09'
method: generated
source: openapi/linkagi-model-api-openapi.json + https://docs.linktoagi.com/codex-api.html
---

# Point Codex at LinkAGI and call the Responses route

## 1. Configure the client

The Responses protocol uses a **different base URL shape** from the Anthropic and Gemini routes:

| Setting | Value |
|---|---|
| Base URL | `https://api.linktoagi.com/v1` |
| Protocol | Responses |
| Auth | `Authorization: Bearer <key>` |

The `/v1` segment belongs in the base URL here. Adding it again in the request path — or omitting it —
produces `404 Invalid URL`, which is the single most common failure on this route
(https://docs.linktoagi.com/codex-404-invalid-url.html).

## 2. Choose a model the Codex pools actually carry — `getPublicPricing`

`GET https://api.linktoagi.com/api/pricing`. Codex-oriented models live in the groups named
`Codex | Pro号池`, `Codex | Plus号池` and `Codex | Sale号池`; `usable_group` labels which of those accept
external clients. Pool membership changes — the provider announced `gpt-5.6-terra` / `gpt-5.6-sol` /
`gpt-5.6-luna` being pushed to the Pro pool on 2026-07-17 and told users to migrate off the Sale pool on
2026-08-03 (see `changelog/linkagi-model-api-changelog.yml`).

## 3. Send the call — `createResponse`

`POST https://api.linktoagi.com/v1/responses`

```json
{
  "model": "gpt-5.6-sol",
  "input": "Reply with: LinkAGI Responses ok",
  "stream": false,
  "max_output_tokens": 32
}
```

Required fields: `model`, `input`. `max_output_tokens` must be ≥ 1.

## Rules

- **This is the one route with a second verified sample.** The provider records an authenticated HTTP 200
  with `gpt-5.6-sol` on 2026-08-04. Nothing beyond that single call is verified — not streaming, not tools.
- **401 first, model second.** `401 Invalid token` on this route is usually the environment variable or
  `config.toml` still pointing somewhere else, or a key outside the Codex group — check those before
  changing the model (https://docs.linktoagi.com/codex-401-invalid-token.html).
- Billable, no idempotency key, `429`/`504` handling as in
  `conventions/linkagi-model-api-conventions.yml`.
- Record `x-oneapi-request-id` from the response headers.
