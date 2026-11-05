# EspoCRM administrative boundary packages

Prebuilt public HDX COD-AB records and vector tiles for the
[Administrative Areas extension](https://github.com/rodekruis/espocrm-admin-areas-extension).
Countries are stored directly at the repository root:

| Directory | Country | Records | Administrative levels |
| --- | --- | ---: | --- |
| [ETH](ETH/) | Ethiopia | 1,271 | 0–3 |
| [KEN](KEN/) | Kenya | 338 | 0–2 |
| [UGA](UGA/) | Uganda | 1,863 | 0–4 |
| [SOM](SOM/) | Somalia | 110 | 0–2 |

[catalog.json](catalog.json) contains manifest SHA256 checksums. Each country
contains `manifest.json`, `records.json` and `admin-N.mbtiles`.
Manifests retain source URLs, attribution, licence, boundary caveats, record
counts and file hashes. [verification.json](verification.json) records complete
tile/property verification and coverage of every record at zoom 8.
There are 3,582 records and 15 MBTiles archives (8,323,072 bytes).
Records contain no full-resolution geometry; tiles use simplified polygons at
zooms 0–8. No private CRM records or indicators are included.

## Extension catalogue

Use this directory URL in **Administration > Administrative Areas > Country packages**:

```text
https://raw.githubusercontent.com/rodekruis/espocrm-admin-boundaries/main
```

This repository is private. Anonymous requests return HTTP 404.
Private downloads require authenticated-download support in the extension and
a fine-grained GitHub token restricted to this repository with
**Contents: read-only** permission. Never commit tokens or put them in URLs.
Moving the files does not by itself enable anonymous downloads.

The extension reviews existing records and geodata before offering to keep or
replace them. Matching record IDs and CRM links are preserved during replacement.
Obsolete linked records must be reassigned first.

## Data licence and caveats

These derived data are licensed under
[CC BY 3.0 IGO](https://creativecommons.org/licenses/by/3.0/igo/legalcode),
not the extension's code licence. Retain attribution, licence and source caveats
when displaying or redistributing them.

- Ethiopia: CSA and regional BoFED; OCHA/HDX. Two contested gazetteer woredas
  lack polygons and are not fabricated as records.
- Kenya: IEBC; OCHA/HDX. Operationally endorsed, not an official national
  administrative layer; admin2 does not conform to COD-PS.
- Uganda: Uganda Bureau of Statistics with WHO; OCHA/HDX. The 135-district
  system; ambiguous lower-level labels are preserved.
- Somalia: OCHA Somalia; OCHA/HDX. Only standard admin0/1/2 polygons; auxiliary
  operational layers are excluded.

**Boundary disclaimer:** The boundaries and names shown and the designations
used on this data do not imply official endorsement or acceptance by the
United Nations.

Full caveats and source descriptions are retained in each manifest.
The extension repository contains the pilot build and verification tools;
keep their local output separate from the extension's published code.
