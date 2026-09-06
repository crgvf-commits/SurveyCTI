# CTI-Sharing Systematic Review — Replication Data Package

This directory contains machine-readable artifacts derived from the manuscript:

**Cyber Threat Intelligence Sharing: An Evidence-Qualified Systematic Review of Solutions and Operational Maturity**

The package is intended to support traceability of the WorldCIST 2027 submission and to allow readers to inspect the included corpus, cluster assignments, evidence rubric, consolidated evidence results, and reported trade-offs without requiring the conference paper to print the complete primary-study bibliography.

## Scope

The manuscript reports:

- 903 records identified;
- 898 records after deduplication;
- 611 records excluded during title/abstract screening;
- 287 full texts assessed;
- 115 full texts excluded;
- 172 primary studies included.

The search window is reported as 2021–2026. The manuscript also states that no eligible 2026 primary study was retained and that the empirical synthesis is concentrated in 2021–2025.

All bibliographic metadata in this package was taken from the manuscript bibliography/BibTeX source. No external bibliographic corrections were introduced when generating these files.

## Files

| File | Purpose |
|---|---|
| `included_studies.csv` | Master list of the 172 included primary studies, with bibliographic metadata and the traceability group/cluster listed in the manuscript. |
| `cluster_assignments.csv` | Compact study-to-group/cluster mapping for analysis or filtering. |
| `cluster_summary.csv` | The 20-cluster solution landscape and the number of studies assigned to each cluster. |
| `evidence_rubric.csv` | E0–E5 and NR evidence definitions, typical evidence, and exclusion conditions. |
| `global_evidence_summary.csv` | Corpus-level evidence summary for effectiveness, adoption, impact, and scalability. |
| `cluster_evidence_summary.csv` | Consolidated cluster-level evidence maxima reported in the manuscript's direct-answer table. |
| `evidence_dense_clusters.csv` | Maximum and median evidence levels for the ten clusters identified as having the highest evidence density. |
| `tradeoffs.csv` | Recurring trade-offs and applicability conditions reported by the synthesis. |
| `data_quality_flags.csv` | Source-data and manuscript inconsistencies that should be verified before public release. |

## Taxonomy

The solution landscape contains four analytical groups and 20 clusters:

- **G1 — Conceptual artifacts:** C1–C5
- **G2 — Technical artifacts:** T1–T7
- **G3 — Interoperability:** I1–I4
- **G4 — Representation and semantics:** S1–S4

The manuscript describes G1–G4 as analytical facets. However, the published traceability tables in the current manuscript version list each of the 172 included studies in exactly one G1–G4 cluster. The CSV files reproduce the traceability tables as written and do not infer additional cross-group memberships.

## Evidence interpretation

Evidence is assessed independently across four axes:

- effectiveness;
- adoption;
- impact;
- scalability.

The ordinal scale ranges from **E0** (no evaluation) to **E5** (robust longitudinal or scale evidence), with **NR** used when no verifiable textual basis is reported.

`cluster_evidence_summary.csv` contains **cluster-level consolidated maxima**, not study-level evidence codes. A maximum can therefore be driven by a small subset of studies and should be interpreted together with medians and counts where available.

`evidence_dense_clusters.csv` contains the maxima and medians reported for the ten evidence-dense clusters: C2, C3, T1, T2, T4, T5, T6, I3, S1, and S2.

## Important limitation: study-level E0–E5 matrix

The current manuscript source does not contain the complete 172 × 4 study-level evidence matrix. Therefore, this package does **not** reconstruct or infer study-level effectiveness, adoption, impact, or scalability values.

The full study-level matrix should only be added from the original structured extraction dataset (for example, the Evidentia Review export or the authoritative consolidated extraction file).

## Data-quality checks before public release

`data_quality_flags.csv` records issues detected in the current source without silently correcting them. These include malformed author metadata, one bibliography year outside the declared search window, two DOI strings embedded in note fields with unusual formatting, and an inconsistency in the manuscript regarding I2 adoption evidence.

The package should be treated as a **draft replication package** until these flags are resolved against the authoritative extraction and bibliographic sources.

## Reproducibility principle

The package follows the manuscript's anti-inference principle: values not explicitly supported by the source material are not reconstructed from assumptions.

## Suggested citation in the paper

A concise statement can be used in the submission:

> The complete corpus of 172 included primary studies, together with the published cluster assignments, evidence rubric, consolidated evidence summaries, and reported trade-offs, is available in the anonymous replication package.

For double-blind review, the repository and all metadata exposed to reviewers should remain anonymous.
