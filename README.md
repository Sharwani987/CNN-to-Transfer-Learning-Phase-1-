# CNN Image Classification – CIFAR-10

## 📌 Project Overview
This project explores **Convolutional Neural Networks (CNNs)** for image classification using the **CIFAR‑10 dataset**.  
It is part of the assignment *“CNN to Transfer Learning”* – Phase 1 focuses on building custom CNNs from scratch, analyzing dataset properties, and experimenting with architectural variations.

---

## 📂 Dataset
- **Source**: CIFAR‑10 (open‑source benchmark dataset)
- **Classes**: 10 (airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck)
- **Images per class**: 6,000 (balanced dataset)
- **Image dimensions**: 32×32×3 (RGB)
- **Total images**: 60,000 (50,000 train + 10,000 test)

---

## 🎯 Problem Statement
- **Goal**: Classify images into one of 10 categories.  
- **Importance**: Image classification is a fundamental computer vision task, widely used in autonomous systems, healthcare, and security.  
- **Expected Output**: Predicted class label for each input image.

---

## ⚙️ Data Preprocessing & Augmentation
- **Resizing**: Images standardized to 32×32×3.  
- **Normalization**: Pixel values scaled to `[0,1]`.  
- **Augmentation Techniques**:
  - Horizontal flipping
  - Width/height shifting
  - Rotation
  - Zoom
  - Brightness/contrast adjustments  

**Why augmentation?**  
It increases dataset diversity, reduces overfitting, and improves generalization.

---

## 📊 Evaluation Metrics
- **Accuracy** – overall performance.  
- **Precision, Recall, F1‑score** – class‑wise performance.  
- **Confusion Matrix** – error distribution across classes.  

⚠️ Limitation: Accuracy alone may hide class imbalance or misclassification trends.

---

## 🏗️ CNN Model Variations
### Variation 1 – Baseline CNN
- Simple 3‑layer CNN, no BatchNorm/Dropout.  
- **Result**: ~10% accuracy → underfitting.

### Variation 2 – Deeper CNN + BatchNorm
- More Conv layers, BatchNormalization, larger Dense layer.  
- **Result**: ~71% validation accuracy.  
- **Behavior**: Strong learning, slight risk of overfitting.

### Variation 3 – Regularized CNN (Dropout + BatchNorm)
- Conv blocks with Dropout + BatchNorm.  
- **Result**: ~60% validation accuracy.  
- **Behavior**: Balanced training/validation → reduced overfitting.

---

## 📈 Results Comparison

| Variation | Training Accuracy | Validation Accuracy | Behavior |
|-----------|------------------|---------------------|----------|
| Baseline CNN | ~10% | ~10% | Underfitting |
| Deeper CNN + BN | ~69.7% | ~71.7% | Good learning, slight overfitting |
| Regularized CNN | ~59.3% | ~59.9% | Stable generalization |

---

## 🔎 Key Takeaways
- **Baseline CNN** underfits and fails to learn.  
- **Deeper CNN** achieves high accuracy but risks overfitting.  
- **Regularized CNN** trades peak accuracy for stability and generalization.  
- Augmentation + normalization are critical for CNN performance.

---

## 🚀 Next Phase
Phase 2 will extend this work to **Transfer Learning** using pretrained models (e.g., VGG16, ResNet, MobileNet) and compare them against custom CNNs.

---

## 📜 License
Open‑source project for educational purposes.
