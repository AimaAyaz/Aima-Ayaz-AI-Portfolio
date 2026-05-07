# 📘 Module 03 — CNNs for Image Classification: Puppy or Bagel?  
**Course:** ITAI 2376 — Deep Learning  
**Student:** Aima Ayaz  
**Date:** Spring 2026  

---

## 🔹 Overview  
This project explores **Convolutional Neural Networks (CNNs)** through a fun and challenging dataset:  
**“Puppy or Bagel?”** — inspired by the viral meme showing how curled‑up puppies resemble bagels.

The goal of this module was to:  
- Understand CNN architecture  
- Build a custom CNN from scratch  
- Apply transfer learning using pre‑trained models  
- Perform data augmentation  
- Evaluate model performance using accuracy, confusion matrices, and classification reports  

---

## 🔹 Dataset  
**Source:** Kaggle — *Puppy or Bagel Dataset*  
- Two classes: **bagel** and **puppy**  
- Small dataset → required augmentation to prevent overfitting  
- Split into:  
  - 80% training  
  - 10% validation  
  - 10% testing  

---

## 🔹 Part 1 — Custom CNN From Scratch  
### **Architecture Built:**  
- **Conv2D (32 filters)** → ReLU → MaxPooling  
- **Conv2D (64 filters)** → ReLU → MaxPooling  
- **Conv2D (128 filters)** → ReLU → MaxPooling  
- **Conv2D (128 filters)** → ReLU → MaxPooling  
- **Flatten**  
- **Dense (512)** → ReLU  
- **Dropout (0.5)**  
- **Dense (1)** → Sigmoid  

### **Key Concepts Learned:**  
- How convolution filters detect edges, textures, and shapes  
- How pooling reduces spatial size and noise  
- How dense layers make final predictions  
- How dropout prevents overfitting  

### **Training Details:**  
- Image size: 150×150  
- Batch size: 32  
- Epochs: 15  
- Optimizer: Adam  
- Loss: Binary Crossentropy  

---

## 🔹 Part 2 — Transfer Learning  
To improve accuracy on a small dataset, transfer learning was applied using:  
- **MobileNetV2**  
- **ResNet50**  

### **Steps Taken:**  
- Loaded pre‑trained ImageNet weights  
- Froze base layers  
- Added custom classification head  
- Fine‑tuned final layers  

### **Benefits Observed:**  
- Faster convergence  
- Higher accuracy  
- Better generalization  

---

## 🔹 Data Augmentation  
Used `ImageDataGenerator` to expand dataset variety:  
- Rotation  
- Width/height shift  
- Shear  
- Zoom  
- Horizontal flip  
- Rescaling  

This significantly reduced overfitting and improved model robustness.

---

## 🔹 Results  
### **Custom CNN:**  
- Good performance but prone to overfitting due to small dataset  

### **Transfer Learning Models:**  
- Achieved higher accuracy  
- More stable validation performance  
- Better feature extraction  

### **Evaluation Metrics:**  
- Accuracy  
- Confusion matrix  
- Classification report  

---

## 🔹 Reflection  
This module strengthened my understanding of CNNs and image classification workflows.  
I learned how:  
- Convolution and pooling layers extract visual features  
- Transfer learning boosts performance on small datasets  
- Data augmentation improves generalization  
- Model evaluation reveals strengths and weaknesses  

The “Puppy vs Bagel” challenge was a fun and effective way to practice real‑world computer vision techniques.

---

## 📁 Files Included  
- `custom_cnn.ipynb` — CNN built from scratch  
- `transfer_learning_mobilenet.ipynb`  
- `transfer_learning_resnet.ipynb`  
- Training logs, accuracy curves, confusion matrices  
- Sample predictions and visualizations  


