# Morphological Image Processing and Color Segmentation

This project explores **mathematical morphology, binary-mask refinement, and color-based segmentation** with OpenCV. It demonstrates how simple image-processing operations can convert noisy visual data into useful object masks.

## Goal

The notebook presents three practical image-processing workflows:

1. Fill black holes inside white circular objects with morphological closing.
2. Segment four skin-lesion images and use opening, closing, erosion, dilation, flood filling, and connected components to remove noise, fill holes, and separate touching lesions.
3. Detect the green clothing in a color image using HSV thresholding, refine its mask, and recolor the detected garment red.

## Setup and usage

Python 3.10 or newer is recommended.

```bash
python -m venv .venv
```

Activate the environment, then install the dependencies:

```bash
python -m pip install -r requirements.txt
jupyter notebook image_processing.ipynb
```

Run the cells in order from the repository root. The notebook reads inputs from `data/` and writes generated segmentation results to `outputs/`.

## Domain overview

Mathematical morphology studies the shape and structure of objects in images. Its fundamental operations—erosion and dilation—can be combined into opening and closing. Opening is commonly used to remove small foreground artifacts, while closing fills small gaps and reconnects nearby regions.

Binary segmentation separates an object of interest from its background. In medical-image analysis, morphology can refine preliminary lesion masks by removing noise, filling internal holes, and separating touching regions. In color images, HSV thresholding offers a practical way to isolate objects by hue while reducing sensitivity to brightness changes.

Connected-component analysis complements these methods by identifying distinct regions in a binary mask. Together, thresholding, morphology, flood filling, and component analysis form a compact pipeline for cleaning masks and extracting meaningful image regions.

## Methods used

- Otsu and fixed-value binary thresholding
- HSV color segmentation
- Morphological opening and closing
- Erosion and dilation
- Flood-fill hole filling
- Connected-component analysis

## Author

Hasti Ebrahimzadeh — Student ID 40133401

This repository is intended for educational demonstration and portfolio use.

