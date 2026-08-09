---
name: Use the LinkAGI Anthropic-style and Gemini-style routes
description: Send Anthropic Messages-shaped and Gemini generateContent-shaped requests through the LinkAGI relay, with the per-route auth headers, and treat both as advertised-but-unverified surfaces rather than guaranteed compatibility.
api: openapi/linkagi-model-api-openapi.json
operations:
  - getPublicStatus
  - getPublicPricing
  - createAnthropicMessage
  - generateGeminiContent
generated: '2026-08-09'
method: generated
source: openapi/linkagi-model-api-openapi.json + https://docs.linktoagi.com/claude-code-api.html + https://docs.linktoagi.com/gemini-cli-api.html
---

# Use the LinkAGI Anthropic-style and Gemini-style routes

**Read this first.** LinkAGI's own OpenAPI marks both of these routes as *advertised, not verified*: the
paths reach authentication without a key, but no authenticated success sample is published for native
Anthropic Messages or Gemini `generateContent`. Treat a first call on either route as a compatibility test,
not a production dependency, and keep the sample small.

## 0. Check the service state — `getPublicStatus`

`GET https://api.linktoagi.com/api/status` (unauthenticated). `data.announcements[]` is where channel and
model retirements are announced — two ClaudeCode channels were retired on 2026-07-21 with no notice window.

## 1. Anthropic-style Messages — `createAnthropicMessage`

`POST https://api.linktoagi.com/v1/messages`

| Header | Value |
|---|---|
| `x-api-key` | `<key>` — **not** `Authorization: Bearer` |
| `anthropic-version` | `2023-06-01` (required) |
| `content-type` | `application/json` |

```json
{
  "model": "<copy a current claude model id from /api/pricing>",
  "max_tokens": 32,
  "messages": [{"role": "user", "content": "Reply with: LinkAGI Messages ok"}]
}
```

For Claude Code, set `ANTHROPIC_BASE_URL=https://api.linktoagi.com` — the host only, no `/v1`. The client
appends `/v1/messages`. A `model not found` here is almost always a group problem
(https://docs.linktoagi.com/claude-code-model-not-found.html).

## 2. Gemini-style generateContent — `generateGeminiContent`

`POST https://api.linktoagi.com/v1beta/models/{model}:generateContent`

| Header | Value |
|---|---|
| `x-goog-api-key` | `<key>` |
| `content-type` | `application/json` |

The model id is a **path** parameter, not a body field. For Gemini CLI set
`GOOGLE_GEMINI_BASE_URL=https://api.linktoagi.com`. A `403` on this route means auth, model permission, or
upstream rejection — verify the base URL and the header name before anything else
(https://docs.linktoagi.com/gemini-cli-403-error.html).

## 3. Pick the model — `getPublicPricing`

Only models whose `supported_endpoint_types` includes `anthropic` (respectively `gemini`) can be addressed
on these routes, and only from a group listed in that model's `enable_groups`.

## Rules

- **Three routes, three different auth headers.** Bearer for the OpenAI routes, `x-api-key` for Anthropic,
  `x-goog-api-key` for Gemini. Sending the wrong one is a 401 or 403, not a 400.
- **No idempotency key.** Retries are billable.
- **Do not present these routes as verified Anthropic/Gemini compatibility** in anything you generate; the
  provider explicitly does not claim it.
- Errors: `{"error":{"code":"","message":"...","type":"new_api_error"}}` — see
  `errors/linkagi-model-api-problem-types.yml`.
