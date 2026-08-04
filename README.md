# University of Leeds (university-of-leeds)

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

The University of Leeds is a public research university in Leeds, United Kingdom, ranked #60 in the QS World University Rankings 2025 and a member of the Russell Group. This repository catalogs the institution's public developer/API footprint as an [APIs.json](https://apisjson.org) profile for the API Evangelist network. Leeds has no central self-service developer portal; its clearest public, machine-readable surface is the Libraries' research data and digital collections infrastructure.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/university-of-leeds/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=university-of-leeds-api-evangelist&utm_content=repo

## Type

- Index
- Consumer
- 3rd-Party

## Tags

Education, Higher Education, University, United Kingdom, Research Data, Libraries, OAI-PMH, IIIF

## APIs

- **Research Data Leeds Repository (OAI-PMH)** — EPrints 3 institutional research data repository; live OAI-PMH 2.0 endpoint for metadata harvesting. Docs: https://archive.researchdata.leeds.ac.uk/ — Base: https://archive.researchdata.leeds.ac.uk/cgi/oai2
- **Cultural Collections IIIF** — Libraries' Cultural Collections IIIF-enabled via a Digirati-built digital library (IIIF Image API + OCFL); manifests discovered per catalogue record. Docs: https://library.leeds.ac.uk/info/1500/special_collections
- **Library Search (Ex Libris Alma / Primo)** — Discovery and resource management on Alma/Primo; programmatic access only via vendor-gated Alma/Primo APIs. Docs: https://library.leeds.ac.uk/info/1100/search-resources

## Plans

See [plans/university-of-leeds-plans-pricing.yml](plans/university-of-leeds-plans-pricing.yml).

## Rate Limits

See [rate-limits/university-of-leeds-rate-limits.yml](rate-limits/university-of-leeds-rate-limits.yml).

## FinOps

See [finops/university-of-leeds-finops.yml](finops/university-of-leeds-finops.yml).

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://www.leeds.ac.uk/
- GitHub: https://github.com/uol-library
- LinkedIn: https://www.linkedin.com/school/university-of-leeds/
- Review: [review.yml](review.yml)

## Notes

All endpoints were probed on 2026-06-03 and no endpoints were fabricated. The OAI-PMH endpoint was verified live (HTTP 200 on `verb=Identify` and `verb=ListMetadataFormats`). IIIF manifests exist but are discovered per catalogue record — no published developer reference or fixed manifest base URL was confirmed. Alma/Primo APIs are vendor-provided and require institution-issued keys; Leeds publishes no public developer docs for them. `data.leeds.ac.uk` is a third-party data consultancy (not the university's open-data portal) and returned HTTP 403 to automated requests; the legacy `id.leeds.ac.uk` linked-open-data host now 301-redirects away with no live API confirmed.

## Maintainers

- Kin Lane — kin@apievangelist.com
