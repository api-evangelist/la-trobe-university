# La Trobe University (la-trobe-university)

La Trobe University is a public research university in Melbourne, Victoria, Australia, ranked #217 in the QS World University Rankings 2025. This repository catalogs La Trobe's public, verifiable developer/API footprint as an [APIs.json](https://apisjson.org) provider profile. La Trobe has no single consolidated public developer portal; its most clearly public, documented machine interface is the OPAL open-access research repository, hosted on Figshare, which exposes a REST API and an OAI-PMH endpoint.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/la-trobe-university/refs/heads/main/apis.yml
- Run it with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=la-trobe-university-api-evangelist&utm_content=repo

## Type

- Index / Consumer / 3rd-Party

## Tags

Education, Higher Education, University, Australia, Research, Open Data, Repository, Library

## APIs

- **OPAL (Open @ La Trobe) Figshare REST API** — institution-scoped (institution=234) access to La Trobe open-access publications, theses, datasets, and educational resources. Docs: https://docs.figshare.com/ — Base: `https://api.figshare.com/v2`
- **OPAL OAI-PMH Endpoint** — metadata harvesting for the La Trobe OPAL portal set (portal_234) via the Figshare OAI provider. Docs: https://docs.figshare.com/#oai_pmh — Base: `https://api.figshare.com/v2/oai`
- **La Trobe API Gateway (Gated)** — an institutional gateway at `api.latrobe.edu.au` exists but redirects unauthenticated traffic to a sign-in page; not a public, self-service, or documented product. Listed for transparency only.

## Plans, Rate Limits, and FinOps

- Plans / Pricing: [plans/la-trobe-university-plans-pricing.yml](plans/la-trobe-university-plans-pricing.yml)
- Rate Limits: [rate-limits/la-trobe-university-rate-limits.yml](rate-limits/la-trobe-university-rate-limits.yml)
- FinOps: [finops/la-trobe-university-finops.yml](finops/la-trobe-university-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://www.latrobe.edu.au/
- LinkedIn: https://www.linkedin.com/school/la-trobe-university/
- Twitter: https://twitter.com/latrobe
- Plans: plans/la-trobe-university-plans-pricing.yml
- Rate Limits: rate-limits/la-trobe-university-rate-limits.yml
- FinOps: finops/la-trobe-university-finops.yml
- Review: review.yml

## Notes

Verification discipline: no endpoints were fabricated. The Figshare REST and OAI-PMH endpoints were probed live and returned La Trobe data (HTTP 200). The OPAL platform (Figshare) is confirmed via the re3data registry entry (r3d100013575). The official website and library hosts return 403 to automated requests (bot protection) but are live in browsers. `developer.latrobe.edu.au` and `data.latrobe.edu.au` do not resolve. The `api.latrobe.edu.au` gateway returns HTTP 302 to a sign-in page and is not publicly documented. Library discovery runs on Ex Libris Alma/Primo. There is no official central La Trobe GitHub organization (only departmental/student groups such as CDAC-lab and gdglatrobe), so no GitHub common property is asserted.

## Maintainers

- Kin Lane — kin@apievangelist.com
