# Cross-session motor-imagery EEG benchmark

This repository provides the reproduction materials for Xinpeng Zheng's study,
*Cross-Session Evaluation of Classical and Compact Decoders for Four-Class
Motor-Imagery EEG*. The work is an offline computational benchmark using BCI
Competition IV data set 2a, not a new laboratory or clinical data collection.

## Download and reproduce

Download `BCICIV2a_Reproducibility_PrivacyReviewed.zip` and verify it against
`SHA256SUMS.txt`. The unchanged archive contains **128 members**. Its SHA-256 is:

```text
a52bffded768ae640047679a5c3fef2b83ecef5f6b1e997d60ca4afd1719b06f
```

Extract it into a new working directory and retain its folder structure. Follow
the extracted `README.md` for dependencies, data acquisition, result audits, and
training commands. `SHA256SUMS.json` inside the ZIP checks the individual files.
Stored predictions and metrics can be audited without retraining; full training
requires separately obtained EEG data and the documented environment.

The archive includes the five scripts listed below, protocols, dependency pins,
experiment results, trial-level predictions, statistical analyses, audit records,
literature notes, and derived EA covariance/whitening matrices. Source-only and
batch-transductive EA conditions are distinguished in the documentation. The
revision analyses are exploratory, not prospectively preregistered.

## Code license and its scope

Effective **2026-10-02**, Xinpeng Zheng authorizes the following five
project-written Python scripts under the root [MIT License](LICENSE). Paths are
relative to the extracted archive root:

- `reproducibility/run_cross_session_benchmark.py`
- `reproducibility/validate_final_results.py`
- `revision_20260921/experiments/run_revision_baselines.py`
- `revision_20260921/experiments/audit_revision_results.py`
- `revision_20260921/analysis/analyze_revision.py`

The MIT grant applies only to these scripts, including their embedded comments
and docstrings, to the extent the author has the right to license them. It does
**not** relicense the BCI dataset, trial-level true-class labels, third-party
dependencies, or other bundled materials. Their existing rights and applicable
terms remain unchanged. This repository grants no additional license to those
excluded materials.

The ZIP is deliberately preserved as a **2026-10-02 pre-license preparation
snapshot**. Its internal statements about private preparation, an unassigned
license, or a deposit not yet made describe that historical snapshot. This root
README and root LICENSE supersede its no-license statements for the five scripts
above from the effective date; they do not alter historical experimental records.
Repository visibility is shown by GitHub, not certified by the archived notes.

The [Motor-Imagery-BCI project](https://github.com/gabfarmarcondes/Motor-Imagery-BCI)
was initially supplied as background. That repository is not bundled here, and
the MIT grant above does not apply to its code.

## Dataset attribution and use

BCI Competition IV data set 2a was provided by the Institute for Knowledge
Discovery (Laboratory of Brain-Computer Interfaces), Graz University of
Technology, Austria. The official dataset description credits C. Brunner,
R. Leeb, G. R. Müller-Putz, A. Schlögl, and G. Pfurtscheller.

Obtain recordings and original evaluation-label archives from the official
sources linked in the extracted README. Review the
[official conditions of use](https://www.bbci.de/competition/iv/#download):
publications analyzing these data must acknowledge the recording group and cite
at least one paper listed in the
[dataset description](https://www.bbci.de/competition/iv/desc_2a.pdf).
One listed paper is:

> C. Brunner, M. Naeem, R. Leeb, B. Graimann, and G. Pfurtscheller,
> “Spatial filtering and selection of optimized components in four class motor
> imagery data using independent components analysis,” *Pattern Recognition
> Letters*, vol. 28, pp. 957–964, 2007.

The organizers also request notification of publications involving competition
data. These dataset conditions are separate from the software license above.

## Privacy and preserved evidence

No raw EEG recordings, original evaluation-label archives, manuscript, teacher
comments, credentials, or third-party software binaries are included. **The
prediction CSVs do contain true-class labels** for metric verification; derived
EA matrices are not raw EEG trials.

Experimental scripts, predictions, and reported metrics were not changed during
publication preparation. Only machine-specific directory strings in three
existing record files were redacted:

1. `reproducibility/results_final_ensemble/run_metadata.json`
2. `reproducibility/results_final_ensemble/run_stdout.log`
3. `revision_20260921/experiments/results/run_metadata.json`

The ZIP's `PUBLICATION_PREPARATION.md` and `REDACTION_RECORD.json` document the
changes and original/publication checksums. Original experimental records remain
preserved separately. The privacy check was bounded in scope, not a universal
security guarantee. This repository is not evidence of conference acceptance or
EI indexing.
