# Concrete Crack Segmentation & Quantification with Mask R-CNN

**Progressive M0–M4 Framework | Research Showcase & Code Repository**

**Dat-Thanh Nguyen · Nhat-Quang Tran · Duc-Hoc Tran**

*Journal of Building Pathology and Rehabilitation*, **11**, Article **228** (2026) · Springer Nature

[**Read the published paper (DOI)**](https://doi.org/10.1007/s41024-026-00900-z) | [**BKAI research website**](https://bkai.b12sites.com/index)

**Keywords:** Concrete cracks · Mask R-CNN · ResNet-50-FPN · PointRend · Skeletonization · Structural health monitoring

---

## About this repository

This repository introduces an integrated Mask R-CNN framework for automated concrete crack segmentation and image-based geometric characterization. It accompanies the peer-reviewed paper published in *Journal of Building Pathology and Rehabilitation* (2026).

**This README is a research showcase, not a replacement for the paper.** For complete experimental settings, statistical analysis, ablation results, and discussion, please [read the full journal article](https://doi.org/10.1007/s41024-026-00900-z).

## Research highlights

- **Progressive instance-aware pipeline:** Mask R-CNN followed by crack-oriented proposals, fine-boundary refinement, topology refinement, and geometric characterization.
- **Controlled evaluation:** Distinct experimental protocols for M0–M4 development and comparison with DeepLabV3+ and YOLOv8m-Seg.
- **Practical demonstration:** BKAI Web/App presents crack masks, image-based measurements, visualization, and reporting.

The contribution is the **systematic integration and evaluation** of established components, rather than claiming the individual algorithms as new inventions.

## Proposed framework

![Progressive development of the M1–M4 framework](assets/images/bkai_paper_2026/fig06_progressive_m1_m4.png)

| Stage | Main purpose |
| --- | --- |
| **M0** | Baseline Mask R-CNN with ResNet-50 and FPN |
| **M1** | Crack-oriented proposal adaptation |
| **M2** | PointRend boundary refinement |
| **M3** | Morphological topology refinement |
| **M4** | Skeleton-based geometric characterization |

**Measurement note:** The M4 outputs are image-domain crack descriptors. Length and width in pixels are not absolute physical measurements unless suitable scale information or calibration is available.

## Selected published results

The paper uses **two separate experimental protocols**. The results below refer only to the **controlled TEST1007** comparison, not the augmented M0–M4 development dataset.

| Metric | M3 result (TEST1007) |
| --- | ---: |
| Precision | **88.69%** |
| Recall | **84.07%** |
| F1-score / Dice | **86.32%** |
| Intersection over Union (IoU) | **75.94%** |

![Controlled model comparison on TEST1007](assets/images/bkai_paper_2026/fig20_test1007_comparison.png)

For statistical uncertainty, detailed ablation studies, and full comparison tables, see the [published paper](https://doi.org/10.1007/s41024-026-00900-z).

## Visual demonstrations

### Concrete crack predictions

![Concrete crack detection and instance-mask examples](assets/images/bkai_paper_2026/fig15_crack_prediction_examples.png)

### Progressive segmentation examples

![Qualitative comparison of M0 through M3](assets/images/bkai_paper_2026/fig17_m0_m3_qualitative_masks.png)

## BKAI Web/App demonstration

The BKAI prototype illustrates an engineering-oriented workflow from uploading images to visualizing predicted cracks and preparing structured inspection outputs. It should not be interpreted as independently validated physical measurement software.

![BKAI Web/App demonstration workflow](assets/images/bkai_paper_2026/fig21_bkai_web_workflow.png)

Project links: [BKAI website](https://bkai.b12sites.com/index) · [BKAI AI application repository](https://github.com/ndtnguyen260696/bkai-ai-app)

## Repository code and reproducibility

The repository contains research notebooks and supporting material. The availability and compatibility of pretrained weights, dataset access, dependencies, and complete reproduction commands must be checked against the actual files in the repository before use. No end-to-end reproducibility claim is made here.

For an implementation overview, browse the repository's `Model/`, `notebooks/`, and `results/` directories as available. For full scientific specifications, refer to the paper.

## Publication and citation

**Nguyen, D.-T., Tran, N.-Q., & Tran, D.-H. (2026).** An integrated mask R-CNN framework for concrete crack segmentation and skeleton-based quantification in automated infrastructure inspection. *Journal of Building Pathology and Rehabilitation, 11*, Article 228.

**DOI:** https://doi.org/10.1007/s41024-026-00900-z

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

## Publication rights and acknowledgments

Please consult the Springer Nature publication agreement before redistributing the publisher-formatted PDF or journal figures. Repository code and other assets may have different applicable licenses; refer to the actual `LICENSE` file and source attribution.

---

**Interested in the methodology, experiments, and scientific discussion? [Read the full Springer Nature article](https://doi.org/10.1007/s41024-026-00900-z).**
