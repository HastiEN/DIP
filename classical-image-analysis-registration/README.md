# Classical Image Analysis and Registration

This project presents a collection of classical computer-vision techniques implemented with Python, NumPy, Matplotlib, and OpenCV. It focuses on the mathematical ideas behind alignment, matching, thresholding, feature detection, and region-based segmentation.

## Domain overview

Image registration aligns two images into a common coordinate system. Landmark-based registration estimates a geometric transformation from corresponding points, while intensity-based registration optimizes transformation parameters by minimizing differences between overlapping images. These techniques are widely used in medical imaging, remote sensing, and multi-view analysis.

Template matching searches for a small reference pattern inside a larger image. Sum of squared differences measures pixel error directly, while normalized cross-correlation measures similarity after normalization and is typically more tolerant of brightness variation.

Image segmentation assigns pixels to meaningful regions. Otsu's method derives a global threshold by maximizing separation between intensity classes. Seeded region growing expands from selected pixels according to an intensity-similarity rule, making spatial connectivity part of the segmentation process.

Feature detection converts image structures into compact geometric representations. Canny detection extracts likely boundaries, and the Hough transform maps edge pixels into a parameter space where prominent straight lines appear as accumulator peaks.

## Demonstrations

The notebook contains six sections:

1. Landmark-based affine alignment of MRI images
2. SSD and NCC template matching
3. Gradient-descent affine registration
4. Manual implementation of Otsu thresholding
5. Canny edges and Hough line detection
6. Multi-seed region-growing segmentation

## Project structure

```text
.
├── image_analysis.ipynb  # Main interactive notebook
├── data/                 # Input images
├── docs/                 # Supporting reference document
├── requirements.txt      # Python dependencies
└── README.md
```

## Setup

Python 3.10 or newer is recommended.

```bash
python -m venv .venv
python -m pip install -r requirements.txt
jupyter notebook image_analysis.ipynb
```

Run the notebook from the repository root. The landmark-registration and region-growing sections open native OpenCV windows and require mouse input, so they should be run in a local desktop environment rather than a headless notebook server.

