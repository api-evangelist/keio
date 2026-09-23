# Keio University (keio)

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

Keio University (慶應義塾大学) is a private research university in Tokyo, Japan, founded by Fukuzawa Yukichi in 1858 and the oldest institution of modern higher education in the country. Its programmable footprint is small, entirely non-commercial, and — unusually for this cohort — genuinely its own rather than a vendor's running under its name.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/keio/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=keio-api-evangelist&utm_content=repo

## Type

- university / Private Research University
- Index
- Consumer
- 3rd-Party

## Tags

Education, Higher Education, University, Japan, Research, Institutional Repository, Research Repository, Identity Federation, Digital Collections, IIIF, OAI-PMH, Open Access, Cultural Heritage

## Surfaces, by who operates them

Every surface below carries an `x-operator` in `apis.yml`. For a university that distinction is the
whole point: almost every machine-readable thing that appears under an institution's name is a
vendor's contract, and crediting the institution for it is the error this profile exists to avoid.

### Institution-operated — Keio's own hosts, Keio's own engineering

- **KOARA OAI-PMH Metadata API** — the institutional repository's OAI-PMH 2.0 harvesting interface, live and anonymous. All six verbs probed; 100 faculty and research-centre sets; `oai_dc` and NII `junii2`.
  - Base URL: https://koara.lib.keio.ac.jp/xoonips/modules/xoonips/oai.php
  - Contract: [openapi/keio-koara-oai-pmh-openapi.yml](openapi/keio-koara-oai-pmh-openapi.yml)
- **Keio Media Center Digital Collections IIIF API** — IIIF Presentation 2.1 manifests and IIIF Image 2.0 Level 1 tiles for the university's digitised rare books, including all 656 folios of its Gutenberg 42-line Bible. The largest genuinely institution-operated machine-readable surface Keio has.
  - Manifests: https://dcollections.lib.keio.ac.jp/sites/default/files/iiif/
  - Images: https://iiif.lib.keio.ac.jp/
  - Contract: [openapi/keio-iiif-openapi.yml](openapi/keio-iiif-openapi.yml)

### Federation — shared by definition, and the IdP inside it is Keio's

- **Keio University Identity Provider** — entityID `https://gakunin1.keio.ac.jp/idp/shibboleth`, registered in GakuNin since 2014-02-24 and republished into eduGAIN as entity 853677.
  - Detail: [identity-federation/keio-identity-federation.yml](identity-federation/keio-identity-federation.yml)

### Tenant — Keio's data and users, a vendor's contract

- **K-RIS** (k-ris.keio.ac.jp) — Elsevier Pure. Pure's contract is deliberately not saved here; on this deployment `/ws/api` returns 404 anyway.
- **Keio Okta tenant** (keio.okta.com) — OIDC discovery is publicly readable, client registration is not reachable by an outsider.
- **Keio Figshare** (keio.figshare.com) — evidenced through DataCite client `keio.figshare`, not through the host, which bot-interstitials scripted clients.

### Registry — memberships, recorded as facts about Keio, never as Keio's contracts

- **DataCite** — provider `keio`, prefix 10.71825, FSCO consortium, joined 2025-03-11, 5 DOIs minted.
- **Crossref** — member 1082 (Keio Journal of Medicine, prefix 10.2302, 1,743 DOIs) and member 1443 (Department of Anatomy, prefix 10.2535).
- **ROR** — https://ror.org/02kn6nx58.

## Artifacts

- OpenAPI: [KOARA OAI-PMH](openapi/keio-koara-oai-pmh-openapi.yml) · [IIIF](openapi/keio-iiif-openapi.yml) (pristine copies in [openapi/_original/](openapi/_original/))
- JSON Schema: [IIIF manifest](json-schema/keio-iiif-manifest-schema.json) · [IIIF image info](json-schema/keio-iiif-image-info-schema.json)
- [Examples](examples/index.yml) — nine verbatim captured responses
- [Conformance](conformance/keio-conformance.yml) · [Identity federation](identity-federation/keio-identity-federation.yml)
- [Authentication](authentication/keio-authentication.yml) · [Scopes](scopes/keio-scopes.yml) · [Errors](errors/keio-errors.yml)
- [Rules](rules/keio-rules.yml) · [Vocabulary](vocabulary/keio-vocabulary.yml) · [Lifecycle](lifecycle/keio-lifecycle.yml) · [Agentic access](agentic-access/keio-agentic-access.yml)
- [JSON-LD](json-ld/keio-context.jsonld) · [Plans](plans/keio-plans-pricing.yml) · [Rate limits](rate-limits/keio-rate-limits.yml) · [FinOps](finops/keio-finops.yml)

## Domain-standard conformance (Kin Score `education` regime)

Confirmed from live responses, never from a prose claim: **oai-pmh** 2.0 (institution),
**shibboleth** (institution), **saml** 2.0 (institution), **datacite** (registry), **crossref**
(registry). **orcid** is recorded as *partial* — 4,503 affiliation records exist in the public
registry, but no Keio-side integration or membership was found, and inflating that to confirmed
would credit the institution for its researchers' filing behaviour. **scim**, **lti**, **oneroster**,
**ed-fi**, **caliper** and **qti** were probed and not found, and are listed as such rather than
omitted.

## Timestamps

- Created: 2026-06-03
- Modified: 2026-09-01

## Common Properties

- Website: https://www.keio.ac.jp/en/
- Library: https://www.lib.keio.ac.jp/en/
- Research repository: https://koara.lib.keio.ac.jp/
- Digital collections: https://dcollections.lib.keio.ac.jp/en
- AI policy: https://www.st.itc.keio.ac.jp/en/software_ai_guideline.html
- Privacy policy: https://www.keio.ac.jp/en/privacy-policy/
- News: https://www.keio.ac.jp/en/news/
- X: https://x.com/Keio_univ_PR
- LinkedIn: https://www.linkedin.com/school/keio-university
- Instagram: https://www.instagram.com/keio_university
- YouTube: https://www.youtube.com/user/keiouniversity

## Notes

- Every contract in this repository was written by API Evangelist from live probes on 2026-09-01 and is marked `method: derived` in its own `x-provenance` block. **Keio publishes no OpenAPI, AsyncAPI, apis.json or WADL anywhere in its estate.**
- What Keio does not have was probed, not assumed: `api.keio.ac.jp` and `data.keio.ac.jp` do not resolve; there is no developer portal, open-data portal, public course-catalog API, research-computing service catalog, changelog, status page, `llms.txt`, MCP server, `robots.txt` on the main site, or `security.txt`.
- The `github.com/keio` account belongs to an unrelated individual. The `KeioUniversity` and `keio-sfc` GitHub organizations both exist but hold **zero public repositories**, so neither is claimed as a pointer.
- The previous `https://twitter.com/Keio_PR_eng` pointer returned HTTP 404 and was removed; the replacement handle was read off Keio's own English homepage.
- The entityID host `gakunin1.keio.ac.jp` presents an **expired TLS certificate**. It does not break federation — a SAML entityID is an identifier, not a fetch target — but it is recorded as an open defect.
- No endpoints were fabricated. Where a value could not be confirmed (the IIIF archive codes for collections other than Gutenberg), it is left unenumerated rather than guessed.

## Maintainers

- Kin Lane — kin@apievangelist.com
