# LinkAGI Model API

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

**Areas:** Artificial Intelligence · LLM · AI API Gateway · Relay · OpenAI-Compatible · Anthropic Compatible · Gemini-compatible · Developer Tools · CLI coding agents · Model Routing · China

## LinkAGI Model API on APIs.io

Everything profiled for LinkAGI Model API is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/linkagi-model-api/](https://apis.io/providers/linkagi-model-api/)** — or go straight to one of the APIs or properties below.

### APIs (5)

- [LinkAGI Model API Anthropic-style route API](https://apis.io/apis/linkagi-model-api/linkagi-model-api-anthropic-style-route-api/) — Messages-shaped route advertised by the service. The route reaches authentication without a key; authenticated native compatibility has not been verified in…
- [LinkAGI Model API Discovery API](https://apis.io/apis/linkagi-model-api/linkagi-model-api-discovery-api/) — Inspect the models visible to the current token group.
- [LinkAGI Model API Gemini-style route API](https://apis.io/apis/linkagi-model-api/linkagi-model-api-gemini-style-route-api/) — generateContent-shaped route advertised by the service. The route reaches authentication without a key; authenticated native compatibility has not been…
- [LinkAGI Model API OpenAI compatible API](https://apis.io/apis/linkagi-model-api/linkagi-model-api-openai-compatible-api/) — OpenAI-compatible Chat Completions and Responses routes.
- [LinkAGI Model API Public metadata API](https://apis.io/apis/linkagi-model-api/linkagi-model-api-public-metadata-api/) — Unauthenticated service status and live pricing metadata.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [linkagi](https://apis.io/servers/linkagi-model-api/linkagi/)

#### Collections (5)

Postman and Open Collection request collections.

- [LinkAGI Anthropic-style route API](https://apis.io/collections/linkagi-model-api/open-linkagi-model-api-anthropic-style-route-api/)
- [LinkAGI Discovery API](https://apis.io/collections/linkagi-model-api/open-linkagi-model-api-discovery-api/)
- [LinkAGI Gemini-style route API](https://apis.io/collections/linkagi-model-api/open-linkagi-model-api-gemini-style-route-api/)
- [LinkAGI OpenAI compatible API](https://apis.io/collections/linkagi-model-api/open-linkagi-model-api-openai-compatible-api/)
- [LinkAGI Public metadata API](https://apis.io/collections/linkagi-model-api/open-linkagi-model-api-public-metadata-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Linkagi Model Api Openapi Overlay](https://apis.io/overlays/linkagi-model-api/linkagi-model-api-openapi-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Linkagi Model Api Authentication](https://apis.io/security/linkagi-model-api/linkagi-model-api-authentication/)
- [Linkagi Model Api Domain Security](https://apis.io/security/linkagi-model-api/linkagi-model-api-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.linktoagi.com/)
- [Documentation](https://docs.linktoagi.com/)
- [Getting started](https://docs.linktoagi.com/codex-api.html)
- [Pricing](https://api.linktoagi.com/pricing)
- [Sign up](https://api.linktoagi.com/register)
- [Support](https://docs.linktoagi.com/about.html#support)
- [Blog](https://docs.linktoagi.com/articles/)
- [Terms of service](https://api.linktoagi.com/user-agreement)
- [Privacy policy](https://api.linktoagi.com/privacy-policy)
- [Status](https://docs.linktoagi.com/status.html)

## API Evangelist rating

**Kin Score 34.0** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 52.5 |
| Contract governance | 4.5 |
| Operational transparency | 36.8 |
| Developer ergonomics | 44.6 |
| Access clarity | 0.0 |

**Agent readiness 24.3** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | verified |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 15.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/linkagi-model-api/](https://apis.io/providers/linkagi-model-api/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for LinkAGI Model API: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/linkagi-model-api/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
