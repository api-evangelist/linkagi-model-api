# LinkAGI Model API (linkagi-model-api)

LinkAGI is a Chinese third-party AI API relay (中转站) that fronts a pool of upstream model accounts behind a single host, api.linktoagi.com, and re-exposes them on three imitated vendor protocols: OpenAI-compatible Chat Completions and Responses, an Anthropic Messages-shaped route, and a Gemini generateContent-shaped route. It is sold to developers running Codex, Claude Code, Gemini CLI and desktop chat clients who want a CNY, prepaid, pay-as-you-go base-URL swap instead of a foreign card and a vendor account. A token belongs to a group (号池) that decides which models it can address and at what billing ratio; the live model and price table is published unauthenticated at /api/pricing. The service runs the open-source New API gateway and publishes a first-party OpenAPI 3.1, APIs.json, llms.txt and Postman collection, plus an unusually candid evidence boundary that marks its Anthropic and Gemini compatibility as advertised but unverified.

**APIs.json:** [https://linkagi-model-api.apievangelist.com/apis.yml](https://linkagi-model-api.apievangelist.com/apis.yml)

## Tags

- AI
- LLM
- AI API gateway
- relay
- OpenAI-compatible
- Anthropic-compatible
- Gemini-compatible
- developer tools
- CLI coding agents
- model routing
- China

## Timestamps

- **Created:** 2026-08-04
- **Modified:** 2026-08-09

## APIs

### LinkAGI Model API Anthropic-style route API

Messages-shaped route advertised by the service. The route reaches authentication without a key; authenticated native compatibility has not been verified in the latest evidence set.

- **Human URL:** [https://docs.linktoagi.com/](https://docs.linktoagi.com/)
- **Base URL:** `https://api.linktoagi.com`

#### Tags

- Anthropic-style route

#### Properties

- [OpenAPI](openapi/linkagi-model-api-anthropic-style-route-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/linkagi-model-api-anthropic-style-route-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/linkagi-model-api-anthropic-style-route-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Data Model](data-model/linkagi-model-api-data-model.yml)

### LinkAGI Model API Discovery API

Inspect the models visible to the current token group.

- **Human URL:** [https://docs.linktoagi.com/](https://docs.linktoagi.com/)
- **Base URL:** `https://api.linktoagi.com`

#### Tags

- Discovery

#### Properties

- [OpenAPI](openapi/linkagi-model-api-discovery-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/linkagi-model-api-discovery-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/linkagi-model-api-discovery-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Data Model](data-model/linkagi-model-api-data-model.yml)

### LinkAGI Model API Gemini-style route API

generateContent-shaped route advertised by the service. The route reaches authentication without a key; authenticated native compatibility has not been verified in the latest evidence set.

- **Human URL:** [https://docs.linktoagi.com/](https://docs.linktoagi.com/)
- **Base URL:** `https://api.linktoagi.com`

#### Tags

- Gemini-style route

#### Properties

- [OpenAPI](openapi/linkagi-model-api-gemini-style-route-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/linkagi-model-api-gemini-style-route-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/linkagi-model-api-gemini-style-route-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Data Model](data-model/linkagi-model-api-data-model.yml)

### LinkAGI Model API OpenAI compatible API

OpenAI-compatible Chat Completions and Responses routes.

- **Human URL:** [https://docs.linktoagi.com/](https://docs.linktoagi.com/)
- **Base URL:** `https://api.linktoagi.com`

#### Tags

- OpenAI compatible

#### Properties

- [OpenAPI](openapi/linkagi-model-api-openai-compatible-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/linkagi-model-api-openai-compatible-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/linkagi-model-api-openai-compatible-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Data Model](data-model/linkagi-model-api-data-model.yml)

### LinkAGI Model API Public metadata API

Unauthenticated service status and live pricing metadata.

- **Human URL:** [https://docs.linktoagi.com/](https://docs.linktoagi.com/)
- **Base URL:** `https://api.linktoagi.com`

#### Tags

- Public metadata

#### Properties

- [OpenAPI](openapi/linkagi-model-api-public-metadata-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/linkagi-model-api-public-metadata-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/linkagi-model-api-public-metadata-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Data Model](data-model/linkagi-model-api-data-model.yml)

## Common Properties

- [M C P Server](mcp/linkagi-model-api-mcp.yml)
- [Overlay](overlays/linkagi-model-api-openapi-overlay.yaml)
- [Domain Security](security/linkagi-model-api-domain-security.yml)
- [Authentication](authentication/linkagi-model-api-authentication.yml)
- [Developer Portal](https://api.linktoagi.com/)
- [Documentation](https://docs.linktoagi.com/)
- [Getting Started](https://docs.linktoagi.com/codex-api.html)
- [Support](https://docs.linktoagi.com/about.html#support)
- [Blog](https://docs.linktoagi.com/articles/)
- [Blog R S S](https://docs.linktoagi.com/feed.xml)
- [Git Hub](https://github.com/16871233/linkagi-api-starter)
- [Pricing](https://api.linktoagi.com/pricing)
- [Sign Up](https://api.linktoagi.com/register)
- [Terms of Service](https://api.linktoagi.com/user-agreement)
- [Privacy Policy](https://api.linktoagi.com/privacy-policy)
- [Status Page](https://docs.linktoagi.com/status.html)
- [Postman](https://www.postman.com/lhs-1-s-team/linkagi-api/collection/8nl8r40/linkagi-api) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [A P Is J S O N](https://docs.linktoagi.com/apis.json)
- [L L Ms Txt](llms/linkagi-model-api-llms.txt)
- [Changelog](changelog/linkagi-model-api-changelog.yml)
- [Lifecycle](lifecycle/linkagi-model-api-lifecycle.yml)
- [Conventions](conventions/linkagi-model-api-conventions.yml)
- [Error Catalog](errors/linkagi-model-api-problem-types.yml)
- [Conformance](conformance/linkagi-model-api-conformance.yml)
- [Packages](packages/linkagi-model-api-packages.yml)
- [Agent Skill](skills/_index.yml)

## Maintainers

**FN:** LinkAGI Support
**Email:** linktoagi@163.com
**URL:** https://docs.linktoagi.com/about.html#support
