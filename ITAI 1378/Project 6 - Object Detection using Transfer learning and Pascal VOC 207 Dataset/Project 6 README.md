# Object Detection Lab

This README documents a project exploring object detection to identify what and where the objects are in a given image.

---

## Problem Statement

Unlike image classification—which only identifies **what** is in an image—object detection identifies **what** is present **and where** it is by drawing bounding boxes around detected objects.

## Approach

This project implemented object detection using normalized bounding box coordinates and IoU scoring:

- **Bounding boxes** were defined using fractions (0–1) to stay resolution-independent and easily scalable.
- **Intersection over Union (IoU)** evaluated how well predicted boxes matched ground truth; an IoU of **0.5** was used as the baseline for a valid detection.
- Calculations used `max(0, …)` to prevent negative width/height values, since IoU should always remain between 0 and 1.
- Experimented with adjusting **detection thresholds** to filter predictions.

## Results

- At **threshold = 0.3**, the model produced ~10 bounding boxes, including many irrelevant or partial detections.
- At **threshold = 0.7**, the model produced only 2 boxes, but they were more meaningful and accurate.
- Precision and recall remained unchanged in early iterations—even when adjusting IoU thresholds or increasing dataset size—indicating model limitations or data constraints.
- Prediction labels were incorrect at a threshold of 0.5.

## Key Findings

- Higher thresholds (e.g., 0.7) reduce noise by eliminating low-confidence detections.
- Classification alone is insufficient for tasks requiring spatial awareness; bounding boxes provide essential context.
- IoU is sensitive to bounding box quality—small coordinate errors can drastically affect scores.
- Application requirements dictate whether **precision** or **recall** should take priority.

## Technologies Used

- Python
- Jupyter/Colab
- PyTorch (improved object detection notebook)

## Real-World Applications

- **Autonomous Vehicles:** Detect and locate pedestrians, vehicles, signs—classification alone cannot provide distance or spatial context.
- **Security Systems:** Track individuals or vehicles across surveillance footage.
- **Inventory Management:** Identify product locations and detect low-stock shelves.

## How to Run

1. Open the notebook file Lab_06_Improved_2025_submission.ipynb in **Google Colab**.
2. Run all cells to generate predictions, bounding boxes, and IoU metrics.
