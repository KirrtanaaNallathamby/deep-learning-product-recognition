# Deep Learning Product Recognition
# CNN vs. ResNet-50: Malaysian Product Recognition (Food Classification)

This repository contains the implementation of a deep learning project focused on classifying five iconic Malaysian food categories: **Nasi Lemak, Laksa, Roti Canai, Popiah, and Satay**. This project was developed as part of the WID3011: Computer Vision module at Universiti Malaya.

## 📌 Project Overview
The primary goal was to compare the performance of a **Custom CNN Architecture** built from scratch against a **Transfer Learning** approach using the **ResNet-50** model.

### Key Objectives:
* Develop a custom CNN with at least 4 convolutional layers.
* Implement a transfer learning model using pre-trained weights from ImageNet.
* Compare models based on accuracy, training time, and convergence speed.
* Analyze misclassifications and propose real-world business applications for Malaysian SMEs.

## 📊 Dataset
The project utilizes the **Malaysia Food 11** dataset from Kaggle.
* **Selected Classes:** Nasi Lemak, Laksa, Roti Canai, Popiah, Satay.
* **Data Split:** 80% Training, 20% Validation.
* **Preprocessing:** Images resized to 224x224, pixel normalization, and data augmentation (rotation, zoom, horizontal flip).

## 🛠️ Model Architectures

### 1. Custom CNN
A sequential model consisting of:
* 4 Convolutional Blocks (Filters: 32, 64, 128, 128)
* Max-Pooling layers for spatial reduction
* Fully Connected (Dense) layer with 128 neurons
* Softmax output layer for 5-class classification

### 2. ResNet-50 (Transfer Learning)
* **Backbone:** Pre-trained ResNet-50 (weights='imagenet')
* **Strategy:** Feature Extraction (base layers frozen)
* **Head:** Global Average Pooling + Dense (128) + Softmax (5)

## 📈 Performance Comparison

| Metric | Custom CNN | ResNet-50 |
| :--- | :--- | :--- |
| **Validation Accuracy** | ~72% | **~90.8%** |
| **Training Time** | Slow | **Fast** |
| **Convergence** | ~15-20 Epochs | **~4-5 Epochs** |

## 🚀 How to Run
1.  Open the provided Colab notebook.
2.  Upload your `kaggle.json` API key.
3.  Run the cells sequentially to download the dataset, train the models, and view the results.

## 🔍 Misclassification Analysis
The models were evaluated using a confusion matrix. Analysis of 10 specific samples showed that the custom CNN often struggled with visually similar textures (e.g., distinguishing gravy types), whereas ResNet-50's pre-trained features provided much higher robustness.

## 💼 Business Application
This system can be deployed in Malaysian SMEs for:
* **Automated Kiosk Systems:** Quick identification of food items for billing in eateries.
* **Dietary Tracking:** Mobile applications tailored to the Malaysian diet for calorie monitoring.

---
**Author:** Kirrtanaa Nallathamby
**Course:** WID3011 - Deep Learning for Business Applications
