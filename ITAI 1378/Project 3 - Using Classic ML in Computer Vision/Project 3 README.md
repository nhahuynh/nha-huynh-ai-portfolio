# Classical Computer Vision for Face Recognition

This README documents a project exploring the classical computer vision for facial recognition.

---

## Problem Statement

The goal is to successfully implement face recognition with limited training data (10 images per person) by converting raw pixel data into effective features, comparing classical ML algorithms, and preventing **overfitting**.

## Approach (Features & Algorithms)

| Step                   | Method/Algorithm                          | Purpose                                  | Resulting Features           |
| :--------------------- | :---------------------------------------- | :--------------------------------------- | :--------------------------- |
| **Feature Extraction** | **HOG** (Histogram of Oriented Gradients) | Captures **shape and structure** (edges) | 1764 dimensions              |
|                        | **LBP** (Local Binary Patterns)           | Captures **texture patterns**            | 10 dimensions (most compact) |
| **Model Training**     | **SVM** (Support Vector Machine)          | Finds optimal separation between classes |                              |
|                        | **Random Forest (RF)**                    | Ensemble method for robust prediction    |                              |

## Results & Key Findings

| Metric              | SVM + HOG            | RF + LBP (Worst) | Overfitting Lesson                           |
| :------------------ | :------------------- | :--------------- | :------------------------------------------- |
| Training Accuracy   | **1.000 (100.0%)**   | 1.000 (100.0%)   | **High Training Accuracy $\neq$ Good Model** |
| Validation Accuracy | **0.963 (96.3%)**    | 0.388 (38.8%)    | **Real-world performance** is what matters   |
| Overfitting Gap     | **0.037 (Smallest)** | 0.613 (Largest)  | A small gap means **better generalization**  |

**Key Finding:** The **SVM model with HOG features** was selected because it achieved the highest validation accuracy and the smallest overfitting gap, proving it **learned general patterns** rather than just memorizing the limited training set.

## Technologies Used

- **Python** (3.x)
- **Scikit-learn (sklearn)**
- **Scikit-image (skimage)** (for HOG and LBP)
- **OpenCV (cv2)**

## How to Run

1.  Open the `L03_A_NhaHuynh_ITAI_1378.ipynb` notebook in Google Colab.
2.  Run all cells sequentially.
