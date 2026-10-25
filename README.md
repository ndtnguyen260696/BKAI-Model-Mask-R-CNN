<div align="center">
Concrete Crack Segmentation & Quantification with Mask R-CNN
Progressive M0–M4 Framework · Research Showcase & Code Repository
Dat-Thanh Nguyen · Nhat-Quang Tran · Duc-Hoc Tran
Journal of Building Pathology and Rehabilitation 11, Article 228 (2026) · Springer Nature
![Read the Paper](https://img.shields.io/badge/Read_the_Paper-Springer_Nature-1769aa?style=for-the-badge)
![DOI](https://img.shields.io/badge/DOI-10.1007%2Fs41024--026--00900--z-4d658b?style=for-the-badge)
Mask R-CNN · ResNet-50-FPN · PointRend · Morphological Refinement · Skeletonization
</div>
> **About this repository.** A concise introduction to the published research and its supporting code and visual demonstrations. **For the complete methodology, experimental settings, statistical analyses, and scientific discussion, please [read the peer-reviewed article](https://doi.org/10.1007/s41024-026-00900-z).** This page is not intended to reproduce the publication.
Research overview
Automated inspection of concrete infrastructure requires more than locating cracks: irregular crack regions must be segmented and described in an interpretable manner. This research integrates Mask R-CNN with a progressive, instance-aware refinement workflow, M0 → M1 → M2 → M3 → M4, to improve crack-mask representation and support subsequent geometric characterization. The study evaluates the framework using curated concrete-crack imagery, compares its segmentation results with established architectures under a controlled test protocol, and demonstrates an inspection-oriented BKAI Web/App workflow.
What the work contributes
Progressive instance-aware processing: proposal adaptation, boundary refinement, and topology refinement built upon a common Mask R-CNN baseline.
Controlled evaluation: separate component-level and cross-model experiments to characterize the benefits and trade-offs of the framework.
Inspection-oriented outputs: refined masks connected to crack-wise image-domain geometry, visualization, and reporting.
The scientific contribution is the integration and evaluation of existing techniques—not a claim that Mask R-CNN, PointRend, morphology, or skeletonization were invented in this study.
Framework at a glance
<p align="center">
  <img src="assets/images/bkai_paper_2026/fig06_progressive_m1_m4.png" alt="Progressive M1 to M4 crack-analysis stages" width="780">
</p>
Stage	Role
M0	Baseline Mask R-CNN with ResNet-50-FPN
M1	Crack-oriented region-proposal adaptation
M2	PointRend fine-boundary refinement
M3	Morphological topology refinement
M4	Skeleton- and distance-based geometric characterization
M4 produces image-based crack descriptors. Without a scale reference or camera calibration, pixel-derived length and width must not be presented as absolute physical dimensions.
Selected results
The published study uses two distinct experimental protocols. Development experiments use a training-augmented dataset; the separate controlled comparison is performed on a fixed TEST1007 subset. The figures below are illustrative highlights; full tables, ablation details, and uncertainty analysis appear in the paper.
M3 on the controlled TEST1007 protocol:
Precision	Recall	F1-score / Dice	IoU
88.69%	84.07%	86.32%	75.94%
<p align="center">
  <img src="assets/images/bkai_paper_2026/fig20_test1007_comparison.png" alt="Controlled comparison of M0, M3, DeepLabV3+, and YOLOv8m-Seg" width="760">
</p>
The comparison is specific to the study's controlled test protocol; results should not be compared directly with metrics from the separately augmented development protocol.
Visual demonstrations
Crack detection and instance-mask examples
<p align="center">
  <img src="assets/images/bkai_paper_2026/fig15_crack_prediction_examples.png" alt="Examples of concrete crack detection and mask overlays" width="760">
</p>
Qualitative progression from M0 to M3
<p align="center">
  <img src="assets/images/bkai_paper_2026/fig17_m0_m3_qualitative_masks.png" alt="Qualitative crack-mask comparison across M0, M1, M2, and M3" width="660">
</p>
BKAI Web/App demonstration
The research is accompanied by a BKAI inspection workflow for image-based crack analysis, visualization of predicted regions, and structured inspection reporting. The interface illustrates a research prototype; it should not be interpreted as independently validated, calibrated physical measurement software.
<p align="center">
  <img src="assets/images/bkai_paper_2026/fig21_bkai_web_workflow.png" alt="BKAI Web/App research demonstration workflow" width="760">
</p>
BKAI Research Website
BKAI AI App repository
Research dataset page
Availability of external demos, datasets, and trained weights may vary. Dataset reuse is governed by the respective source terms.
Code and reproducibility
This repository accompanies the article. The availability of notebooks, configurations, dependencies, model weights, and end-to-end reproduction commands has not yet been independently verified for this README edition. Please inspect the repository contents before running code; do not assume the published models can be fully reproduced solely from this page.
For experimental protocols, implementation details, and results, consult the full journal article. If executable instructions and checkpoints are released, they should be documented here with their actual file paths and software versions.
Publication and citation
Nguyen, D.-T., Tran, N.-Q., & Tran, D.-H. (2026). An integrated mask R-CNN framework for concrete crack segmentation and skeleton-based quantification in automated infrastructure inspection. Journal of Building Pathology and Rehabilitation, 11, Article 228.
DOI: https://doi.org/10.1007/s41024-026-00900-z
```bibtex
@article{Nguyen2026IntegratedMaskRCNN,
  author  = {Nguyen, Dat-Thanh and Tran, Nhat-Quang and Tran, Duc-Hoc},
  title   = {An integrated mask R-CNN framework for concrete crack segmentation and skeleton-based quantification in automated infrastructure inspection},
  journal = {Journal of Building Pathology and Rehabilitation},
  year    = {2026},
  volume  = {11},
  pages   = {228},
  doi     = {10.1007/s41024-026-00900-z}
}
```
Publication and image rights: Please check the Springer Nature publication agreement before redistributing journal-formatted figures or the publisher PDF. The figures included here were supplied for preparing this repository; their public redistribution rights should be confirmed before upload. The repository's existing `LICENSE` governs only material it actually covers; do not assume it supersedes the journal agreement or third-party dataset licenses.
---
<div align="center">
Interested in the full methods, quantitative experiments, and discussion?
Read the published paper on Springer Nature
</div>
