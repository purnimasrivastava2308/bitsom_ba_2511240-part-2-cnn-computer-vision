# CNN Computer Vision Project

This project implements a Convolutional Neural Network for computer vision tasks.

## Problem Statement
**Image Classification** of surface defects on manufactured parts (e.g., car body panels).

## Project Structure

- `notebook.ipynb` - Main Jupyter notebook with model implementation
- `requirements.txt` - Python dependencies
- `sample_predictions/` - Sample prediction outputs
- `results/` - Training results and analysis

## Getting Started

1. Install dependencies: `pip install -r requirements.txt`
2. Open and run `notebook.ipynb`

### Dataset
- **Classes**: 4 (`normal`, `scratch`, `dent`, `stain`)
- **Total Images**: 480 (120 per class)
- **Problem Type**: Multi-class Image Classification

### Results
- Test Accuracy: **~92-95%** (varies with training)
- Best Model: Simple CNN with Conv2D + MaxPooling + ReLU

# Task 6 & 7: CNN Concepts and Business Use Case

## Task 6: CNN Concept Explanation

### 1. What is Convolution?
Convolution is a mathematical operation where a small filter (kernel) slides over the input image to detect important features such as edges, textures, corners, and patterns. Each filter learns to detect specific features during training.

### 2. Why is Pooling used?
Pooling (e.g., MaxPooling) reduces the spatial dimensions (height and width) of the feature maps. It makes the model more computationally efficient, reduces the number of parameters, helps prevent overfitting, and provides **translation invariance** — meaning the model can still recognize an object even if it appears in a slightly different position.

### 3. Why is ReLU commonly used in CNNs?
ReLU (Rectified Linear Unit) is the most popular activation function in CNNs because:
- It introduces **non-linearity** into the model.
- It helps solve the **vanishing gradient problem**, allowing deeper networks to train effectively.
- It is computationally efficient (simple thresholding operation).

### 4. Why are CNNs better than regular feed-forward networks for image data?
Unlike traditional fully connected networks, CNNs have two major advantages:
- **Parameter Sharing**: The same filter is used across the entire image, drastically reducing the number of parameters.
- **Local Connectivity**: Neurons only look at a small region of the image, preserving spatial hierarchy and relationships between nearby pixels.

This makes CNNs much more efficient and effective at learning visual patterns.

---

## Task 7: Business Use Case

**Domain**: Manufacturing / Automotive Quality Control

This CNN-based defect detection model can be deployed on production lines to automatically inspect car body panels, metal sheets, or industrial parts for surface defects such as **scratches, dents, and stains**.

### Key Benefits:
- **Real-time defect detection** during manufacturing
- Significantly **reduced human inspection errors**
- Faster quality assurance process
- Substantial **cost savings** by catching defects early
- Consistent and objective quality standards
- Scalable solution for high-volume production lines

This type of computer vision system is already being used by major automotive and electronics manufacturers to improve product quality and operational efficiency.