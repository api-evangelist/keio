# Keio University (keio)

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
