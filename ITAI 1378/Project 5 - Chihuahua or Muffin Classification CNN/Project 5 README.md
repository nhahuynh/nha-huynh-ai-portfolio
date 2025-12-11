# Chihuahua vs. Muffin Classification Using CNNs

This README documents a project exploring image classification of chihuahua dogs and muffins using convolutional neural network.

--

## Problem Statement

The goal of this project is to accurately classify images as either **chihuahuas** or **muffins**, a task known for its visual ambiguity. Traditional neural networks struggled with this classification, so this project applies a **Convolutional Neural Network (CNN)** to improve efficiency and accuracy.

## Approach

I implemented a CNN architecture designed to preserve spatial relationships in images. Key components included:

- **Convolutional layers** to detect local features (edges, textures, shapes)
- **Pooling layers** to downsample feature maps and improve efficiency
- **Fully connected layers** for final classification

This architecture contrasts with a traditional neural network that flattens images and loses spatial information, making CNNs far more suited to vision tasks.

## Results

Using 64×64 images and training for **10 epochs**:

- The CNN achieved a **96% accuracy** (misclassified 1 image out of 24)
- Repeated runs misclassified the _same_ image, even when increased to 15 epochs
- Training time was significantly faster than the traditional NN
- Outperformed the previous NN-based model, which required far more parameter tuning without reaching comparable accuracy

## Key Findings

- CNNs excel at preserving spatial hierarchies that traditional NNs lose, making them far more accurate and efficient for image classification.
- Certain edge-case images may continue to confuse the model, highlighting the importance of dataset diversity.
- Strong model performance can be achieved quickly with minimal tuning when using the right architecture.
- Faster training time and higher accuracy make CNNs ideal for visually complex tasks.

## Technologies Used

- **PyTorch**
- **Python**
- **Pillow (PIL)** for image loading
- Jupyter/Colab environment

## Challenges

This experiment went smoothly with no runtime errors—benefiting from experience gained in the previous workshop.

## Ethical Considerations

- **Model bias** can persist if not addressed (e.g., the repeatedly misclassified chihuahua).
- When models are retired, training data must be properly deleted or anonymized.
- Users should have a secure, transparent way to request deletion of data used in model training.

## Real-World Applications

CNNs are widely used in:

- **Medical imaging** (tumor detection, cell classification)
- **Quality control** in manufacturing
- **Autonomous vehicles** for object detection
- Any domain where accuracy and throughput are critical

## How to Run

1. Open notebook file L05_NhaHuynh.ipynb in **Google Colab**
2. Run the cells to build and evaluate the CNN classifier.
