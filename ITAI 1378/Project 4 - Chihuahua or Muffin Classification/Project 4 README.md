# Chihuahua vs. Muffin Image Classification

This README documents a project exploring the image classification between chihuahua dogs and muffins using a neural network.

--

## Problem Statement

Distinguishing between chihuahuas and muffins is a classic image-classification challenge due to their similar visual features. This project aims to build a neural network capable of correctly classifying images into these two categories.

## Approach

I used **PyTorch** to build and train a neural network classifier. The workflow included:

- Converting images into **tensors**
- Training over multiple **epochs**
- Calculating loss using **Cross-Entropy Loss**
- Optimizing model parameters with **Stochastic Gradient Descent (SGD)**
- Experimenting with different image sizes and epoch counts to improve performance

## Results

After iterative experimentation, the best performance came from using **64×64 images** and training for **15 epochs**.

- Achieved **~90% accuracy** on most validation images
- Early runs showed class bias depending on image size
- Increasing epochs improved generalization and consistency

## Key Findings

- Neural networks learn best through iterative adjustments; increasing epochs significantly improved results.
- Larger image sizes (e.g., 120×120) introduced noise that hurt accuracy.
- Small changes in preprocessing (image size, scaling) can dramatically shift class bias.
- Debugging code imports (e.g., reimporting `Image`) can resolve unexpected runtime errors.

## Technologies Used

- **PyTorch**
- **Python**
- **PIL (Pillow)** for image loading
- Jupyter/Colab environment

## How to Run

1. Open the notebook L04_NhaHuynh_ITAI_1378.ipynb in **Google Colab**
2. Run the training cells to generate the model and evaluate validation results.
