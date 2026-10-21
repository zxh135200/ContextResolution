# Context-Resolution Allocation for Efficient State-Space Semantic Segmentation

Research code and experimental evidence for **Context-Resolution Allocation for Efficient State-Space Semantic Segmentation**. The public project is named **ContextResolution** and is based on the SegMAN implementation.

## Download the complete code and results

**[Download the complete reproducibility bundle](ContextResolution-code-and-results.zip?raw=true)** (approximately 22 MiB compressed).

The code is distributed as an archive in this repository. Download and extract it to inspect or run the source; GitHub does not automatically expand uploaded ZIP files into a browsable source tree. The extracted `ContextResolution/` directory contains the full runtime, modified study backbone, configurations, immutable raw evidence, numerical tables, provenance, licenses and reproduction scripts.

| Evidence | Included records |
|---|---:|
| SegMAN Cityscapes 160k target training | 50: nine lattice policies and control, five repeats each |
| SegMAN Cityscapes 8k proxy experiments | 45: nine policies, five repeats each |
| SegFormer-B0 Cityscapes 8k transfer | 6: `8421` and `6221`, three repeats each |
| SegMAN ADE20K 160k | 9: three policies, three repeats each |
| Authentic qualitative prediction masks | 45: 15 fixed Cityscapes scenes and three policies |

The Cityscapes policy lattice uses `s1 in {4,6,8}`, `s2 in {2,3,4}` and stages 3-4 fixed to 1; `1111` is the control. The archive includes the complete 19-class Cityscapes IoU table, policy rankings, proxy-to-target correlations, shortlist regret, resource/Pareto results and existing diagnostic/profiling evidence. Raw files with identical contents are deduplicated by hash; the provenance index maps original source names to the retained files.

## Quick verification

After extracting the downloaded archive, open its `ContextResolution/` directory and run:

```bash
python scripts/verify_results.py
```

This standard-library check verifies 110 principal raw records, logged actual seeds and budgets, numerical statistics, the per-class tables, ranking/regret calculations, profiling source numbers and Pareto frontiers. Portable configurations have been exported for all 110 records. GPU installation and training/inference instructions are in the extracted `README.md` and `docs/` directory. Fresh GPU training was not repeated during release preparation.

The population standard deviation (`ddof=0`) and stability score `S = mean(mIoU) - std(mIoU)` are used. Nominal run labels and logged actual random seeds are separate fields; the archive documents source-selection discrepancies and does not claim a fully paired-seed design. The final `4211` scores selected from the prior submitted archive are `80.56, 80.87, 80.40, 80.61, 80.69` (mean `80.626`).

## Data and checkpoint availability

Original Cityscapes and ADE20K images and annotations are obtained from their official providers under the relevant access and license terms, and are not mirrored here. The archive includes genuine model prediction masks, selected image IDs, fixed crop coordinates and inference settings. Users with an authorized local Cityscapes copy can reconstruct the qualitative panels from the saved predictions.

**Trained checkpoints are not distributed in this release.** Some historical checkpoints were deleted after the experimental evidence and prediction masks were retained. Checkpoint hashes in the archive establish provenance and are not download links. Repeating model inference requires retained matching weights or fresh training; numerical verification of the raw logs and inspection of saved predictions do not require weights.

See [Data and code availability](DATA_AVAILABILITY.md). The archive retains original Apache-2.0 and third-party notices, including the separately licensed NVIDIA SegFormer components with non-commercial research/evaluation restrictions. Dataset terms remain applicable to the external benchmarks.

## Integrity

The SHA-256 checksum of the downloadable bundle is recorded in [SHA256SUMS.txt](SHA256SUMS.txt). The archive additionally contains a per-file manifest and content hashes. Preparation-stage status metadata inside the archive records the local audit date; it is not a live indication of this repository's publication state.

Based on [the official SegMAN implementation](https://github.com/yunxiangfu2001/SegMAN) at commit `ac606438a87d4c4d4b48064df844c86dfbd59958`. Full attribution is retained inside the archive.
