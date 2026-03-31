# Physics-Constrained DSPI Dataset (PC-DSPI)

## Overview
The **Physics-Constrained DSPI Dataset (PC-DSPI)** is a large-scale, high-quality synthetic dataset designed for phase retrieval and denoising tasks in Digital Speckle Pattern Interferometry (DSPI). Built upon rigorous optical interference principles, this dataset provides a robust benchmark for evaluating traditional filtering algorithms and modern deep learning architectures (e.g., PR-UNet) under extreme, non-white speckle noise conditions.

## Key Features
* **Physics-Driven Noise Modeling:** Unlike standard additive Gaussian noise, the speckle noise in this dataset is synthesized based on real-world coherent optical principles, accurately reflecting the severe degradation seen in practical DSPI measurements.
* **Complex Topological Modes:** The dataset includes a wide variety of phase topographies, ranging from simple Gaussian bumps to complex, higher-order mechanical vibration modes and high-frequency dense fringes.
* **Paired Ground Truth:** Every noisy wrapped phase map is strictly paired with its noise-free wrapped phase and absolute unwrapped phase, enabling end-to-end training and quantitative evaluation.

## Dataset Structure
To facilitate direct integration with deep learning pipelines (e.g., PyTorch DataLoaders), the dataset is pre-split into training and validation sets. The directory structure is organized as follows:

```text
PC-DSPI/
├── train/                  # Training set
│   ├── clean/              # Noise-free phase maps (Ground Truth)
│   └── noise/              # Highly degraded wrapped phase maps (Model Input)
└── val/                    # Validation set
    ├── clean/              # Noise-free phase maps (Ground Truth)
    └── noise/              # Highly degraded wrapped phase maps (Model Input)
## Applications
This dataset is highly suitable for tasks involving:
* Extreme noise filtering in interferometry.
* Deep learning-based phase unwrapping.
* Structural health monitoring and dynamic deformation analysis.

## Citation
If you find this dataset or the associated PR-UNet model useful in your research, please consider citing our paper:
> [Yuanming Ren], "A Physics-Constrained Phase Retrieval Network for Phase Map Denoising in DSPI", *Mechanical Systems and Signal Processing* (Under Review), 2026.
