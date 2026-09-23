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

The University of Leeds is a public research university in Leeds, United Kingdom, and a member of
the Russell Group. This repository is an independent [APIs.json](https://apisjson.org) profile of the
institution's **public, machine-readable footprint**, maintained by API Evangelist and re-profiled
on **2026-08-30** under the API Evangelist university pipeline.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/university-of-leeds/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=university-of-leeds-api-evangelist&utm_content=repo

## Who operates what

A university is a federation of buyers, so the first question about any surface here is not *is
there a spec* but **who runs the thing the spec describes**. Every entry in `apis.yml` carries an
`x-operator`.

| Surface | Operator | Why |
|---|---|---|
| Research Data Leeds Repository (OAI-PMH) | `institution` | `archive.researchdata.leeds.ac.uk` → `roadmap4.leeds.ac.uk` (129.11.190.31). Self-hosted EPrints. |
| Leeds Digital Library (OAI-PMH + OpenSearch) | `institution` | `digital.library.leeds.ac.uk` → 129.11.78.169, Leeds address space. Self-hosted EPrints. |
| Spacefinder campus space data | `institution` | `spacefinder.leeds.ac.uk`; app and data authored by `github.com/uol-library`. |
| Library floor plans IIIF Image API | `institution` | `floorplans.library.leeds.ac.uk` → `lib-sc-prd.leeds.ac.uk` (129.11.190.52). |
| Library Search (Ex Libris Alma / Primo) | `tenant` | Runs at `leeds.primo.exlibrisgroup.com` with view id `44LEE_INST`. Vendor host, vendor contract, vendor keys. |
| White Rose Research Online (OAI-PMH) | `tenant` | `eprints.whiterose.ac.uk` — a three-university consortium platform shared with Sheffield and York. |

No vendor specification is stored under this slug, and none should be. The two tenant entries are
recorded as **relationships**, because a tenancy is a real institutional fact and one of the few
programmable surfaces most universities have — but the engineering is not Leeds'.

## What is actually callable

All four institution-operated surfaces are anonymous, keyless and read-only. Verified live on
2026-08-30:

- **`https://archive.researchdata.leeds.ac.uk/cgi/oai2`** — OAI-PMH 2.0. Six metadata prefixes
  (`oai_dc`, `didl`, `mets`, `oai_bibl`, `rdf`, `uketd_dc`), earliest datestamp 2023-07-27,
  `deletedRecord: persistent`. Datasets carry DataCite DOIs under the university's own `10.5518`
  prefix.
- **`https://digital.library.leeds.ac.uk/cgi/oai2`** — a second, separate EPrints instance holding
  digitised Special Collections, plus an **OpenSearch 1.1** description offering Atom and BibTeX.
- **`https://spacefinder.leeds.ac.uk/spaces.json`** — 68 campus study spaces with geolocation,
  per-weekday opening hours, facilities, noise, atmosphere and accessibility. 137,649 bytes, no key.
- **`https://floorplans.library.leeds.ac.uk/assets/iiif/…/info.json`** — IIIF Image API **level 0**,
  1024×1024 tiles, four libraries in `original` and `cropped` variants.

**The four OpenAPI documents in `openapi/` were derived by API Evangelist from those probes.** The
University of Leeds publishes no OpenAPI, no developer portal, no API gateway, no status page and no
changelog. `https://www.leeds.ac.uk/llms.txt` returns 404.

## What changed in the 2026-08-30 re-profile

- **Ex Libris Alma/Primo re-labelled `tenant`.** It previously carried a `library.leeds.ac.uk`
  `humanURL`, which made a vendor tenancy read as institution-owned to any host-based verdict.
- **"Cultural Collections IIIF" withdrawn.** Its own 2026-06-03 description admitted no confirmed
  manifest base URL. The EPrints manifest endpoint at
  `digital.library.leeds.ac.uk/cgi/iiif/manifest/{id}` is a **soft-200** — HTTP 200 with a
  **zero-byte body** for identifiers 1, 2, 100, 500, 1000 and 1705. Replaced with the library floor
  plans IIIF service, which was verified.
- **The `data.leeds.ac.uk` "third-party data consultancy" note was wrong** and is removed. The host
  is under the university's own registrable domain, resolves to WP Engine, and is Cloudflare
  bot-challenged (HTTP 403 to curl and to a browser user-agent alike). It is `bot_blocked` and
  unread — not third-party.
- **Three new institution-operated surfaces added**: the Digital Library, Spacefinder, and the floor
  plans IIIF service. None of them were in the June profile.
- **Two negative findings recorded** in `conformance/` so they are not re-claimed from prose: no
  publicly retrievable Shibboleth/SAML metadata exists under any `leeds.ac.uk` host
  (`idp.leeds.ac.uk` redirects to a ServiceNow catalogue item), and ORCID is documented for
  researchers but emitted in no machine-readable surface.

## Domain standards (Kin Score `education` regime)

Read from the contract and the wire, never from a claim on a page. See
[conformance/university-of-leeds-conformance.yml](conformance/university-of-leeds-conformance.yml).

| Standard | Conformant | Evidence |
|---|---|---|
| `oai-pmh` | **yes** | two independent institution-operated 2.0 endpoints |
| `datacite` | **yes** | DOI `10.5518/1362` emitted in harvestable `oai_dc` metadata |
| IIIF Image API (non-regime) | **yes** | `"profile": "level0"` on the institution's own host |
| OpenSearch 1.1 (non-regime) | **yes** | description document at `digital.library.leeds.ac.uk` |
| `orcid` | no | documented for researchers, absent from every machine-readable surface |
| `shibboleth` / `saml` | no | no retrievable entity metadata under any `leeds.ac.uk` host |
| `scim`, `lti`, `oneroster`, `ed-fi`, `caliper`, `qti`, `crossref` | no | no surface found |

## Artifacts

| Directory | Contents | Provenance |
|---|---|---|
| `openapi/` (+ `_original/`) | four contracts, one per institution surface | `derived` from probes |
| `json-schema/` | Spacefinder space object | `derived` from the live response |
| `vocabulary/` | every controlled value present in the live Spacefinder data | `derived` |
| `examples/` | verbatim HTTP 200 response bodies | `harvested` |
| `conformance/` | education-regime standards, positive **and** negative | `derived` from probes |
| `authentication/`, `scopes/` | anonymous everywhere; no authorization boundary to scope | `derived` from probes |
| `errors/` | OAI errors arrive at HTTP 200; the soft-200 IIIF endpoint | `derived` from probes |
| `lifecycle/` | no versioning, no changelog, no status page | `derived` from probes |
| `rules/` | consumption rules for integrators | `derived` |

## Notes

Nothing here was fabricated and nothing is attributed to the University of Leeds that the University
of Leeds does not operate. `arc.leeds.ac.uk` (Advanced Research Computing, the Aire HPC service),
`data.leeds.ac.uk` and `generative-ai.leeds.ac.uk` are all live but Cloudflare bot-challenged; they
are recorded as pointers, and their contents were not read. The module and programme catalogue at
`catalogue.leeds.ac.uk` is institution-operated but HTML-only — it is a `CourseCatalog` pointer, not
an API.

## Maintainers

- Kin Lane — kin@apievangelist.com
