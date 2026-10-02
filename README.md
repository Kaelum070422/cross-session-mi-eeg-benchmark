# Cross-session motor-imagery EEG benchmark: private preparation repository

This private repository is being prepared for the reproducibility materials of
Xinpeng Zheng's paper, *Cross-Session Evaluation of Classical and Compact
Decoders for Four-Class Motor-Imagery EEG*.

It is not yet a public code release. No DOI has been assigned, and no software
license has been selected. The materials must not be described as open source
on the basis of this private deposit.

## Files and use

- `BCICIV2a_Reproducibility_PrivacyReviewed.zip`: the scoped reproduction package.
- `SHA256SUMS.txt`: the actual SHA-256 checksum of that ZIP.
- This README: repository status, scope, and handling guidance.

Download the ZIP, optionally verify its checksum against `SHA256SUMS.txt`, and
extract it into a new folder. The extracted `README.md` is at the archive's root;
follow its dependency, data-acquisition, audit, and rerun instructions. Keep the
extracted folder structure intact. The inner `SHA256SUMS.json` verifies the
individual package files.

## Included and excluded

The package includes experiment scripts, protocol/configuration files, pinned
scientific dependencies, reproduction instructions, original and added experiment
results, trial-level predictions, statistical analyses, audit records, derived
EA covariance/whitening matrices, and literature notes. It supports auditing the
stored results without retraining; full training requires separately obtained
data and the documented environment.

It does not include the paper manuscript, teacher review/comments, raw EEG
recordings, raw evaluation-label archives, unrelated personal files, credentials,
or third-party software binaries. The derived EA matrices are not raw EEG trials.
Dataset and third-party rights remain with their respective owners; obtain the
dataset separately from the sources listed in the extracted README and follow
their terms.

## Privacy changes and scientific integrity

The original experimental scripts, protocols, predictions, and reported metrics
are unchanged. Exactly three existing record files had machine-specific absolute
directory strings replaced with explanatory placeholders:

1. `reproducibility/results_final_ensemble/run_metadata.json`
2. `reproducibility/results_final_ensemble/run_stdout.log`
3. `revision_20260921/experiments/results/run_metadata.json`

The extracted `PUBLICATION_PREPARATION.md` and `REDACTION_RECORD.json` explain
these transformations and record original/publication checksums. The package
manifest was regenerated after redaction. The archived original experiment
records were not overwritten. Privacy review was a bounded file-scope and
text-pattern check, not a universal security guarantee.

## Pending before any public release

The author still needs to select an appropriate software license after confirming
code ownership/provenance, and review applicable data-use and submission-anonymity
conditions. No new software license is granted by this README. Only after an
authorized public release should availability wording be updated and an accessible
repository URL or a separately assigned archival DOI be cited in the paper.

Preparing this repository does not constitute journal/conference submission,
acceptance, publication, or EI indexing.
