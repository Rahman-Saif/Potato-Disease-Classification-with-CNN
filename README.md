# 🌿 Plant Disease Classification using Deep Learning

## 📌 Project Overview

This project focuses on classifying plant leaf diseases using a Convolutional Neural Network (CNN). The model is trained on the Plant Village dataset and can identify different plant diseases as well as healthy plant conditions from leaf images. The project demonstrates a complete deep learning pipeline, including data acquisition, preprocessing, model development, training, evaluation, and image classification.

---

<img width="1920" height="1083" alt="image" src="https://github.com/user-attachments/assets/31997dc5-eb9e-44a8-83f3-086f574ec3ba" />

## 🎯 Objectives

* Detect plant diseases from leaf images.
* Classify images into multiple disease categories.
* Build an accurate CNN-based image classification model.
* Support early disease detection for improved agricultural productivity.

---

## 📊 Dataset Information

### Dataset Source

* Plant Village Dataset
* Downloaded using KaggleHub

### Dataset Statistics

| Attribute     | Value     |
| ------------- | --------- |
| Total Images  | 20,638    |
| Total Classes | 15        |
| Image Size    | 128 × 128 |
| Batch Size    | 16        |

The dataset contains images of healthy and diseased plant leaves belonging to multiple crop categories.

---

## 🧹 Data Preprocessing

The dataset was loaded using TensorFlow's image dataset API:

* Automatic class detection from directory structure
* Image resizing to 128×128 pixels
* Batch processing with batch size 16
* Data pipeline optimization using:

  * cache()
  * shuffle(1000)
  * prefetch(tf.data.AUTOTUNE)

---

## 📂 Dataset Splitting

The dataset was divided into training, validation, and testing sets.

### Split Ratio

* Training Set: 64%
* Validation Set: 16%
* Test Set: 20%

### Dataset Distribution

| Dataset    | Batches |
| ---------- | ------- |
| Training   | 825     |
| Validation | 207     |
| Testing    | 258     |

This split ensures unbiased model evaluation on unseen data.

---

## 🧠 CNN Model Architecture

The model was built using TensorFlow Keras Sequential API.

### Architecture

* Input Layer
* Rescaling Layer
* Conv2D (32 Filters, ReLU)
* MaxPooling2D
* Conv2D (64 Filters, ReLU)
* MaxPooling2D
* Conv2D (64 Filters, ReLU)
* MaxPooling2D
* Flatten Layer
* Dense Layer (64 Units, ReLU)
* Output Layer (15 Units, Softmax)

### Model Features

* Feature extraction through convolutional layers
* Spatial downsampling using max pooling
* Multi-class classification using Softmax activation

---

## ⚙️ Model Training

### Training Configuration

| Parameter     | Value                         |
| ------------- | ----------------------------- |
| Optimizer     | Adam                          |
| Loss Function | SparseCategoricalCrossentropy |
| Metric        | Accuracy                      |
| Epochs        | 10                            |
| Batch Size    | 16                            |

---

## 📈 Model Performance

### Training Results

| Metric              | Value  |
| ------------------- | ------ |
| Training Accuracy   | 89.19% |
| Validation Accuracy | 88.85% |
| Training Loss       | 0.3110 |
| Validation Loss     | 0.3297 |

### Test Results

| Metric        | Value  |
| ------------- | ------ |
| Test Accuracy | 88.20% |
| Test Loss     | 0.3394 |

The model achieved strong classification performance with minimal overfitting, as indicated by the close training and validation metrics.

---

## 📊 Training Analysis

Training history plots demonstrated:

* Steady increase in training accuracy
* Consistent validation accuracy
* Decreasing training and validation loss
* Good convergence behavior
* Minimal overfitting

---

## 🛠️ Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Matplotlib
* KaggleHub

---

## 🚀 Results

The CNN model successfully learned discriminative features from plant leaf images and achieved over **88% classification accuracy** on unseen test data.

This demonstrates the effectiveness of deep learning for automated plant disease detection and agricultural monitoring systems.

---

## 🔮 Future Improvements

* Data Augmentation
* Transfer Learning (ResNet, EfficientNet, MobileNet)
* Hyperparameter Optimization
* Real-Time Disease Detection
* Web Deployment using Gradio or Streamlit
* Mobile Application Integration

---

## 📜 Conclusion

This project presents a deep learning-based solution for plant disease classification using leaf images. By leveraging CNN architecture and the Plant Village dataset, the model achieved strong classification performance and demonstrates the potential of AI-powered disease detection systems in modern agriculture.

---
