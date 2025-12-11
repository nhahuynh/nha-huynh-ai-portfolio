## 🖼️ Image Processing Fundamentals

This README documents a project exploring the **fundamentals of image processing** for the purpose of deep learning and how mathematical operations create visual effects.

---

## Problem Statement

To understand how digital images are represented as **numerical data** (matrices) and how common effects (e.g., blur, edge detection) are computationally applied.

## Approach

1.  **Image Representation:** Treated images as numerical matrices (2D for grayscale, 3D/channels for RGB).
2.  **Kernel-Based Filtering:** Used **convolution kernels** (small matrices) to manipulate pixel values.
    - **Gaussian Blur:** Applied a kernel for smoothing.
    - **Sobel Kernel:** Used for **edge detection** by calculating gradients.
3.  **RGB Manipulation:** Directly altered RGB channel values to observe visual changes.

## Key Findings

- Images are fundamentally **numerical values in matrices** (pixels). Color images use **RGB channels**.
- Visual effects require **mathematical computations** involving kernel operations (e.g., convolution) that "slide" over the pixels.
- This knowledge is critical for applications like **autonomous vehicles** (object detection) and **scientific analysis** (cell identification).

## Technologies Used

- **OpenCV**
- **Python**
- **numpy**
- **matplotlib**
- **Pillow**

## How to Run

1. Open Jupyter notebook file L02_Huynh_Nha_ITAI1378.ipynb in Google Colab
2. Run each cell in the script sequentially
