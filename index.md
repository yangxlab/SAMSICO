---
title: Home
---

# SAM-SICO: Semantic-Interactive Clustering Optimization with SAM for Weakly-Supervised Person Search (IEEE TCSVT 2026)

**Xi Yang**, Hexun Zhou, De Cheng*, Menghui Tian, Nannan Wang

*IEEE Transactions on Circuits and Systems for Video Technology (TCSVT)*, vol. 36, no. 4, pp. 5642–5654, 2026

- Paper (DOI): <https://doi.org/10.1109/TCSVT.2025.3636572>
- IEEE Xplore: <https://ieeexplore.ieee.org/document/11268517/>
- BibTeX record (dblp): <https://dblp.org/rec/journals/tcsv/YangZCTW26.html>
- Code: <https://github.com/yangxlab/SAMSICO>

## Abstract

Weakly-supervised person search presents significant challenges when relying solely on bounding-box annotations, particularly due to inter-class confusion from clothing similarity and intra-class variations caused by illumination changes, which severely degrade cross-view matching accuracy. Existing clustering-based methods, constrained by their heavy dependence on color features, frequently produce unreliable pseudo-labels that ultimately limit model performance.

To overcome these limitations, we present **Segment Anything Model-based Semantic-Interactive Clustering Optimization (SAM-SICO)**, a novel framework that integrates the Segment Anything Model's semantic segmentation capability with adaptive clustering optimization for weakly-supervised person search. Our framework harnesses the representational power of the Segment Anything Model (SAM) to enable detector-free semantic feature learning while significantly improving clustering precision.

## Main Contributions

- **Semantic Contour Embedding (SCE)** — leverages SAM's zero-shot segmentation capability to produce highly accurate human body masks.
- **Relation-driven Semantic Feature Interaction (RSFI)** — effectively mitigates clothing-color bias through innovative dynamic affinity matrix construction across multiscale semantic masks and visual features.
- **Adaptive Clustering Optimization (ACO)** — introduces parameter adaptation to optimize intra-class compactness and inter-class separation metrics.

## Results

Experimental results show that the proposed method outperforms existing state-of-the-art approaches on the **PRW** and **CUHK-SYSU** datasets.

## Repository Contents

The released code bundles the training / inference code together with the required libraries:

| Directory | Description |
| --- | --- |
| `configs/` | Configuration files for training and testing |
| `mmdet/`, `mmdetection-2.4.0/` | Detection codebase (based on MMDetection 2.4.0) |
| `mmcv-1.2.6/` | Required MMCV version |
| `MobileSAM-master/` | Lightweight SAM used for semantic contour embedding |
| `tools/`, `jobs/` | Training / testing entry points and job scripts |
| `demo/`, `tests/` | Inference demo and unit tests |
| `setup.py` | Package build script |

## BibTeX

```
@article{YangZCTW26,
  author  = {Xi Yang and Hexun Zhou and De Cheng and Menghui Tian and Nannan Wang},
  title   = {Semantic-Interactive Clustering Optimization With {SAM} for Weakly Supervised Person Search},
  journal = {IEEE Transactions on Circuits and Systems for Video Technology},
  volume  = {36},
  number  = {4},
  pages   = {5642--5654},
  year    = {2026},
  doi     = {10.1109/TCSVT.2025.3636572}
}
```

## Acknowledgements

This work builds upon [MMDetection](https://github.com/open-mmlab/mmdetection), [MMCV](https://github.com/open-mmlab/mmcv) and [MobileSAM](https://github.com/ChaoningZhang/MobileSAM).
