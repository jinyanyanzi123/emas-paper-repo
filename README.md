# EMAS: Edge-Guided Modeling and Axial Independent Scanning Framework for 3D Medical Image Segmentation

> **Status:** repository in preparation — the manuscript is under submission to *Engineering Applications of Artificial Intelligence* (EAAI).

EMAS is a lightweight self-supervised 3D segmentation framework that couples:

- an **Axial Independent Scanning (AIS)** module that decouples volumetric features along three orthogonal axes and performs bidirectional state-space scans with linear O(N) complexity; and
- an **Edge-Guided Masked Volume Modeling (EdgeMVM)** pre-training strategy that reconstructs voxel intensities together with 3D Sobel gradients to preserve anatomical boundaries.

## Availability statement

- **Datasets are not redistributed in this repository.** All three benchmarks are third-party public datasets; please download them from their official sources (table below).
- **The source code (pre-training, fine-tuning, inference) will be uploaded to this repository upon acceptance** of the manuscript.
- **Pre-trained and fine-tuned EMAS weights will also be released here upon acceptance.** Until then, queries are welcome via the journal's submission system.
- Datasets used are cited in the paper; for reproducibility, the paper documents all preprocessing, splits, and evaluation protocols.

### Datasets (official sources)

| Dataset | Source | Notes |
|---|---|---|
| **BTCV** — *Multi-Atlas Labeling Beyond the Cranial Vault* abdomen CT dataset | <https://www.synapse.org/Synapse:syn3193805> | 30 CT volumes, 13 organs (SYNAPSE account required, standard license terms apply) |
| **MSD Spleen** — *Medical Segmentation Decathlon*, Task 09 | <https://medicaldecathlon.com/> | 41 volumes |
| **MSD Liver** — *Medical Segmentation Decathlon*, Task 03 | <https://medicaldecathlon.com/> | 201 volumes (liver + liver-tumor) |

If you use these datasets, please cite their respective publications:

- Landman, B. et al. *Multi-Atlas Labeling Beyond the Cranial Vault: Workshop Challenge.* MICCAI 2015.
- Antonelli, M. et al. *The Medical Segmentation Decathlon.* Nature Communications 13, 4128 (2022).

## Repository layout (after acceptance)

```
emas-paper-repo/
├── code/                 # training & inference
│   ├── train/            # pre-training + fine-tuning entry points
│   ├── inference/        # sliding-window inference on whole volumes
│   └── utils/            # data loaders, transforms (MONAI), metrics
├── weights/              # pre-trained + fine-tuned EMAS weights
├── README.md
└── LICENSE
```

## Requirements

- Python 3.x, PyTorch 2.1, MONAI
- A single 24-GB consumer GPU (NVIDIA RTX 3090) suffices for end-to-end training via mixed precision and gradient checkpointing.

## Citation & contact

Citation details and contact information will be added here upon acceptance.
