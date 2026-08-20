# cloud-itonami-lei-549300mmvl80rtbp3o28

> **Independent third-party archive/analysis. Not affiliated with, endorsed by, or sponsored by SOLVAY.**

This repository archives the publicly published legal notice of **SOLVAY** (BE), with source-url and retrieval-date provenance, per
ADR-2607110300 (`cloud-itonami-lei-corporate-tos-catalog`, `com-junkawasaki/root`).
Read-only reference/archive repository — not a governed Advisor/Governor actor.

- LEI: `549300MMVL80RTBP3O28` (GLEIF entity status ACTIVE, registration ISSUED)
- Source: https://www.solvay.com/en/career/teams/legal
- Retrieved: 2026-07-25T07:01:30Z
- SHA-256 of archived text: `52773de64008741c06ac61f6704031c3079a48abc408162573042564dca24e46`

Acquired by `scripts/lei-acquire.cljs` as part of the worldwide-broadening
continuation that followed the 2026-07-25 coverage audit, which found the
catalog's real reach was 27 countries with the United States at 55%.

## Verified citations

`facts/catalog.edn` records the public-register citations behind this entity.
Every row is checked live — nothing is recorded here that was not retrieved.

```sh
nbb tools/verify_citations.cljs facts/catalog.edn --min 19
```

Exit codes are three-valued on purpose, so that "nothing was checked" and
"nothing was wrong" cannot be confused:

| exit | meaning |
|---|---|
| 0 | every citation fetched 2xx and still carries its claim |
| 1 | at least one citation drifted (named on stderr as `DRIFT <id>`) |
| 2 | the gate could not answer (missing/unparseable catalog, zero checks, below `--min`) |

Three independent authorities are cited, not one:

| authority | rows | what it independently corroborates |
|---|---|---|
| GLEIF | 13 | LEI, legal + HQ address, ELF `R85P`, registration authority, managing LOU, parent reporting exceptions, direct children, ISINs |
| Belgian Crossroads Bank of Enterprises (`kbopub.economie.fgov.be`) | 4 | enterprise number `0403.091.220`, name, start date 1863-12-26, legal form |
| Euronext | 2 | ISIN `BE0003470755` admitted on `XBRU` (Euronext Brussels) |

The CBE rows are what make this more than a GLEIF mirror: the 1863 start date,
the seat and the legal form come from the national register that validated the
LEI, not from GLEIF's copy of it. Note that the CBE search page answers `200`
even for an enterprise number that does not exist, so the substring check —
not the HTTP status — is what actually carries these four rows.

**The entity's own legal page is not a citation row.** `https://www.solvay.com/en/career/teams/legal`
answered when this repository was created (2026-07-25, see the SHA-256 above)
and now returns HTTP 403 to automated clients. That is bot protection, which
this gate does not attempt to work around, so the page is omitted rather than
recorded as a citation the gate cannot check. The archived text and its
retrieval date remain in `80-data/public/tos.journal.edn`.
