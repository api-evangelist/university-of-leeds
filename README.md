# University of Leeds (university-of-leeds)

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
