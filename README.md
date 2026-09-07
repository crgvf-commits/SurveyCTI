# CTI-Sharing Systematic Review — Replication and Traceability Data Package

This repository contains the machine-readable replication and traceability
artifacts associated with the manuscript:

**Cyber Threat Intelligence Sharing: Solutions and Evidence Maturity**

The package accompanies the WorldCIST 2027 submission and supports inspection
of the included corpus, primary group and cluster assignments, evidence rubric,
study-level evidence coding, consolidated evidence results, and recurring
trade-offs reported in the manuscript.

## Scope

The systematic review reports:

- 903 records identified;
- 898 records after deduplication;
- 611 records excluded during title/abstract screening;
- 287 full texts assessed;
- 115 full texts excluded;
- 172 primary studies included.

The search window covers publications from 2021 to 2026 in English or
Portuguese.

The review follows the anti-inference principle described in the manuscript:
when a primary study does not provide a verifiable textual basis for an
analytical field or evidence axis, the value is recorded as NR rather than
inferred.

## Files

| File | Purpose |
|---|---|
| `included_studies.csv` | Master list of the 172 included primary studies, with bibliographic metadata and their primary analytical group and functional cluster. |
| `included_studies.bib` | BibTeX bibliography of the 172 included primary studies, when provided. |
| `cluster_assignments.csv` | Compact mapping between each included study, its primary analytical group, and its primary functional cluster. |
| `cluster_summary.csv` | The 20-cluster CTI-sharing solution landscape and the number of studies assigned to each cluster. |
| `evidence_rubric.csv` | Definitions of E0–E5 and NR, including typical evidence and exclusion conditions. |
| `study_evidence_matrix.csv` | Study-level evidence assignments for effectiveness, adoption, impact, and scalability across the 172 included studies. |
| `global_evidence_summary.csv` | Corpus-level evidence summary reported in the manuscript. |
| `cluster_evidence_summary.csv` | Cluster-level evidence statistics derived from the study-level evidence matrix. |
| `evidence_dense_clusters.csv` | Evidence statistics for the ten clusters identified in the manuscript as having the highest evidence density. |
| `tradeoffs.csv` | Recurring operational trade-offs and applicability conditions identified in the synthesis. |
| `review_bibliography_full.csv` | Machine-readable bibliography associated with the review dataset, comprising the 172 included primary studies and methodological/supporting references used in the extended review source. |
| `review_bibliography_full.bib` | BibTeX version of the review bibliography, when provided. |
| `data_quality_audit.csv` | Optional audit record documenting resolved source-data checks. No unresolved issue should remain in the public review package. |

## Analytical taxonomy

The solution landscape contains four analytical groups and 20 functional
clusters:

- **G1 — Conceptual artifacts:** C1–C5
- **G2 — Technical artifacts:** T1–T7
- **G3 — Interoperability mechanisms:** I1–I4
- **G4 — Representation and semantics:** S1–S4

The review uses faceted coding to characterize heterogeneous CTI-sharing
solutions. For the disjoint aggregation reported in the manuscript and
reproduced in this package, each included study is assigned one **primary
analytical group** and one **primary functional cluster**.

Cross-cutting technologies, standards, and ecosystem elements may be retained
separately as tags and are not counted as additional primary cluster
assignments.

The primary cluster counts sum to the 172 included studies.

## Evidence assessment

Evidence is assessed independently across four axes:

- effectiveness;
- adoption;
- impact;
- scalability.

The ordinal evidence scale ranges from **E0** (no evaluation) to **E5**
(robust longitudinal or scale evidence). **NR** denotes cases for which no
verifiable textual basis was reported in the primary study.

Evidence levels refer to the strength of the evidence reported for each
analytical axis and should not be interpreted as direct measurements of
real-world prevalence.

## Study-level evidence matrix

`study_evidence_matrix.csv` is the authoritative study-level representation
used to support corpus-level and cluster-level evidence summaries.

Each included study has one value for each evidence axis:

- effectiveness;
- adoption;
- impact;
- scalability.

Permitted values are:

`E0`, `E1`, `E2`, `E3`, `E4`, `E5`, and `NR`.

No study-level value should be reconstructed from aggregate statistics.
The matrix must originate from the authoritative structured extraction dataset
used in the review.

## Derived evidence summaries

`global_evidence_summary.csv`, `cluster_evidence_summary.csv`, and
`evidence_dense_clusters.csv` contain aggregated representations of the
study-level evidence data.

Cluster maxima must not be interpreted in isolation. A maximum may be driven
by a single study or a small subset of studies. The manuscript therefore
interprets maxima together with medians, ranges, cluster sizes, and counts of
studies reaching E >= 3 where available.

The ten higher-density evidence clusters discussed in the manuscript are:

`C2`, `C3`, `T1`, `T2`, `T4`, `T5`, `T6`, `I3`, `S1`, and `S2`.

## Reproducibility and traceability

The package is designed to support the following traceability chain:

primary study
→ primary group/cluster assignment
→ study-level evidence coding
→ cluster-level aggregation
→ corpus-level results reported in the manuscript.

Derived values must remain reproducible from the authoritative study-level
files and must not be manually reconstructed from the published aggregate
results.

## Data-quality policy

Bibliographic or analytical discrepancies are resolved against the
authoritative extraction and bibliographic sources before release.

No unresolved data-quality flag should remain in the version exposed to
reviewers.

If `data_quality_audit.csv` is retained, it should document only resolved
checks and the authoritative source used for each resolution.

## Anonymity

This repository is intended for double-blind review.

The repository, file metadata, commit metadata, documentation, paths, comments,
and machine-readable artifacts exposed to reviewers must not contain author
names, affiliations, e-mail addresses, institutional identifiers, personal
usernames, local paths, or links that reveal the identities of the manuscript
authors.

## Suggested statement in the manuscript

> The complete corpus, study-to-cluster mapping, study-level evidence coding,
> evidence summaries, and bibliographic data are available in the anonymized
> replication package.

## Manuscript

**Cyber Threat Intelligence Sharing: Solutions and Evidence Maturity**

Target venue: **WorldCIST 2027**  
Submission category: **Full Paper**
