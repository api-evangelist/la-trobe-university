# La Trobe University (la-trobe-university)

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

La Trobe University is a public research university in Bundoora, Melbourne, Victoria, Australia, ranked #217 in the QS World University Rankings 2025. This repository catalogs La Trobe's public, verifiable developer/API footprint as an [APIs.json](https://apisjson.org) provider profile. La Trobe publishes no API contract of its own — no OpenAPI, AsyncAPI or GraphQL description — and operates no public developer portal. Every surface here carries an `x-operator` saying who actually runs the thing it describes: one institution-operated but sign-in-gated API gateway, and two institutional tenancies on platforms someone else engineered.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/la-trobe-university/refs/heads/main/apis.yml
- Run it with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=la-trobe-university-api-evangelist&utm_content=repo

## Type

- Index / Consumer / 3rd-Party

## Tags

Education, Higher Education, University, Australia, Victoria, Research, Research Repository, Course Catalog, Identity Federation, Library, Open Access

## APIs

- **La Trobe API Gateway (Gated)** — `x-operator: institution`. An Azure API Management instance at `api.latrobe.edu.au` (CNAME `ltu-api-prod-apim.developer.azure-api.net`). Every path — `/apis`, `/developer`, `/.well-known/openid-configuration` — returns the APIM sign-in page. No catalogue, no specification, no open sign-up. Listed for transparency only.
- **OPAL (Open @ La Trobe) Research Repository** — `x-operator: tenant`. La Trobe's open-access repository, deployed on Figshare: `opal.latrobe.edu.au` is a CNAME to `figshare.com` and `researchdata.latrobe.edu.au` redirects to `latrobe.figshare.com`. The data, the DOI prefix `10.26181` and the OAI-PMH set `portal_234` are La Trobe's; the API contract is Figshare's and is scored against Figshare. Set-scoped harvest: `https://api.figshare.com/v2/oai?verb=ListIdentifiers&metadataPrefix=oai_dc&set=portal_234` (HTTP 200, verified 2026-08-30).
- **La Trobe Shibboleth Identity Provider (AAF)** — `x-operator: tenant`. SAML 2.0 metadata served unauthenticated at `https://aaf.latrobe.edu.au/idp/shibboleth` (HTTP 200, application/xml). entityID `https://aaf.latrobe.edu.au/idp/shibboleth`, `shibmd:Scope latrobe.edu.au`, also carried in the AAF federation aggregate and through it into eduGAIN. Marked tenant because `aaf.latrobe.edu.au` CNAMEs to `idp-cname.aaf.edu.au`: the identity namespace is La Trobe's, the Shibboleth deployment is the Australian Access Federation's.

## Plans, Rate Limits, and FinOps

- Plans / Pricing: [plans/la-trobe-university-plans-pricing.yml](plans/la-trobe-university-plans-pricing.yml)
- Rate Limits: [rate-limits/la-trobe-university-rate-limits.yml](rate-limits/la-trobe-university-rate-limits.yml)
- FinOps: [finops/la-trobe-university-finops.yml](finops/la-trobe-university-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-08-30

## Common Properties

- Website: https://www.latrobe.edu.au/
- LinkedIn: https://www.linkedin.com/school/la-trobe-university/
- Twitter: https://twitter.com/latrobe
- Research Repository: https://opal.latrobe.edu.au/
- Course Catalog: https://handbook.latrobe.edu.au/
- Library Catalog: https://latrobe.primo.exlibrisgroup.com/discovery/search?vid=61LATROBE_INST:LATROBE
- Identity Federation: https://aaf.latrobe.edu.au/idp/shibboleth
- Conformance: conformance/la-trobe-university-conformance.yml
- JSON-LD: json-ld/la-trobe-university-context.jsonld
- Domain Security: security/la-trobe-university-domain-security.yml
- Plans: plans/la-trobe-university-plans-pricing.yml
- Rate Limits: rate-limits/la-trobe-university-rate-limits.yml
- FinOps: finops/la-trobe-university-finops.yml
- Review: review.yml

## Notes

Re-profiled 2026-08-30 under the API Evangelist university pipeline, which settles operator attribution before saving any contract.

**What was removed.** The 2026-06-03 profile stored the Figshare REST API v2 under La Trobe's name as two refined OpenAPIs (`articles`, `collections`) plus their pristine source, and every artifact derived from them: OpenCollection and Postman collections, four examples, a JSON Schema, a JSON Structure, two Spectral rulesets, a vocabulary, an agentic-access contract and a capability map. Those documents describe `https://api.figshare.com/v2` with `info.contact: Figshare Support` — the same contract at least five other institutions in this cohort were also credited with. Twenty-one files were removed. Nothing La Trobe authored was deleted, because La Trobe has authored no API contract.

**What survived and what is new.** The OPAL relationship was not deleted, it was re-labelled `x-operator: tenant` — it is a real institutional fact and one of the few programmable surfaces La Trobe has. Newly found and verified: the AAF/eduGAIN Shibboleth identity provider, the CourseLoop-backed course handbook, the Ex Libris Primo discovery layer, and a `conformance/` record for the education-regime domain standards.

**Verification discipline.** No endpoints were fabricated and no OpenAPI was generated for a surface that does not publish one. Every URL asserted here was probed on 2026-08-30. `developer.latrobe.edu.au` and `data.latrobe.edu.au` do not resolve; there is no CKAN or Socrata portal and no institution-hosted OAI-PMH responder (`opal.latrobe.edu.au/oai` answers HTTP 202 with an empty body). The CourseLoop backend (`cf-api-ap-southeast-2.prod.courseloop.com`) refuses unauthenticated calls. Every page on `latrobe.edu.au` sits behind a Cloudflare managed challenge and answers 403 to any non-browser client — including `/robots.txt`, `/llms.txt` and `/.well-known/security.txt` — so no terms, privacy or policy pointer could be verified and none is claimed. Registry identity that *is* La Trobe's own was confirmed directly: DataCite provider `latrobe` with prefix `10.26181` over 47,824 DOIs, Crossref member 11371, ROR 01rxfrp27. There is no official central La Trobe GitHub organization — `LaTrobeUniversity` and `La-Trobe-University` both exist and both hold zero public repositories — so no GitHub pointer is asserted.

**A correction that lowers the score is the pipeline working.** This profile will score lower than the June one did. The June number was Figshare's.

## Maintainers

- Kin Lane — kin@apievangelist.com
