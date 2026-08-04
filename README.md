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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Keio University is a private research university in Tokyo, Japan (founded 1858), ranked #188 in the QS World University Rankings 2025. Its confirmed public, machine-readable footprint centers on KOARA, the institutional repository, which serves a live OAI-PMH 2.0 metadata endpoint. Most other campus systems are account-gated and publish no open developer API documentation.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/keio/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=keio-api-evangelist&utm_content=repo

## Type

- Index
- Consumer
- 3rd-Party

## Tags

Education, Higher Education, University, Research, Institutional Repository, OAI-PMH, Open Access, Japan

## APIs

- **KOARA OAI-PMH Metadata API** — Metadata harvesting for Keio University's institutional repository (XooNips platform, OAI-PMH 2.0).
  - Docs: https://koara.lib.keio.ac.jp/doc/KOARA_About_en.htm
  - Base URL: https://koara.lib.keio.ac.jp/xoonips/modules/xoonips/oai.php

## Plans

- [plans/keio-plans-pricing.yml](plans/keio-plans-pricing.yml)

## Rate Limits

- [rate-limits/keio-rate-limits.yml](rate-limits/keio-rate-limits.yml)

## FinOps

- [finops/keio-finops.yml](finops/keio-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://www.keio.ac.jp/en/
- Library Website: https://www.lib.keio.ac.jp/en/
- Authentication (federation): https://www.gakunin.jp/en
- Twitter: https://twitter.com/Keio_PR_eng
- LinkedIn: https://www.linkedin.com/school/keio-university/

## Notes

- KOARA's OAI-PMH endpoint was verified live (HTTP 200, valid Identify response, protocolVersion 2.0).
- No public REST API or developer portal was found. keio.jp SSO (Google Workspace), Canvas K-LMS, K-RIS, KOSMOS discovery, and the Keio Object Hub are account-gated with no published open API documentation.
- Identity is federated via GakuNin (Japanese academic SAML/Shibboleth federation, participating in eduGAIN).
- The `github.com/keio` account belongs to an unrelated individual developer, not the institution; only research-lab GitHub orgs exist. No endpoints were fabricated.

## Maintainers

- Kin Lane — kin@apievangelist.com
