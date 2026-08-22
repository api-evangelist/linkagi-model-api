# LinkAGI Model API (linkagi-model-api)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
