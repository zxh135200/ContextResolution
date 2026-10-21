# Data and code availability

The experiments use Cityscapes and ADE20K, available from their official providers at <https://www.cityscapes-dataset.com/> and <https://ade20k.csail.mit.edu/>, subject to their respective registration, access and licensing conditions. Original benchmark images and annotations are not redistributed in this repository.

The study code, experimental configurations, available raw logs, per-run and per-class numerical results, profiling records, analysis scripts and authentic qualitative prediction masks are provided in [the complete reproducibility archive](ContextResolution-code-and-results.zip). Image identifiers, crop coordinates, inference settings and source hashes are included to support inspection and reproduction using an authorized local benchmark copy.

Trained checkpoints are not distributed in this release and no public checkpoint download is claimed. Recorded hashes identify the checkpoints used for retained outputs, but do not establish continued checkpoint availability. Some historical weights were deleted after the raw results and predictions were retained. Repeating checkpoint inference requires retained matching weights or fresh training; archived numerical evidence and saved predictions remain available independently.

Dataset terms: [Cityscapes](https://www.cityscapes-dataset.com/license/) and [ADE20K](https://ade20k.csail.mit.edu/terms/). Software and third-party license texts are retained within the archive.

Public repository: <https://github.com/zxh135200/SegMAN-FIXSR>.

When citing this resource in the manuscript, include this repository URL and an identifiable commit or release. No archival DOI is claimed by these files.
