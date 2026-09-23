# examples

Verbatim HTTP 200 response bodies captured by API Evangelist on **2026-08-30** from
institution-operated University of Leeds endpoints. The bytes are the university's; the capture and
the filenames are ours. Nothing here was authored, edited, or synthesised.

| File | Source | Status | Note |
|---|---|---|---|
| `university-of-leeds-research-data-oai-identify-example.xml` | `https://archive.researchdata.leeds.ac.uk/cgi/oai2?verb=Identify` | 200 | verbatim; an XML provenance comment is prepended |
| `university-of-leeds-digital-library-oai-identify-example.xml` | `https://digital.library.leeds.ac.uk/cgi/oai2?verb=Identify` | 200 | verbatim; an XML provenance comment is prepended |
| `university-of-leeds-spacefinder-spaces-example.json` | `https://spacefinder.leeds.ac.uk/spaces.json` | 200 | the FIRST object of the 68-object array, unmodified; re-indented only |
| `university-of-leeds-spacefinder-filters-example.json` | `https://spacefinder.leeds.ac.uk/filters.json` | 200 | the first two of six facet groups, unmodified; re-indented only |
| `university-of-leeds-floorplans-iiif-info-example.json` | `https://floorplans.library.leeds.ac.uk/assets/iiif/original/brotherton-m1/info.json` | 200 | verbatim IIIF Image API level 0 information document |

JSON cannot carry a comment, so the two JSON captures are marked here rather than in the file.
`method: harvested` — the provider's own document, fetched and re-verified.
