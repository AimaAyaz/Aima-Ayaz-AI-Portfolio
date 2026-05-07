# 📘 Module 02 — Neural Network Foundations: From Scratch to Frameworks  
**Course:** ITAI 2376 — Deep Learning  
**Student:** Aima Ayaz  
**Date:** Spring 2026  

---

## 🔹 Overview  
This project explores the foundations of neural networks by building models **from scratch** using NumPy, and then recreating the same concepts using **PyTorch** and **TensorFlow/Keras**.  
The goal of this module was to understand how neural networks work internally before relying on high‑level frameworks.

---

## 🔹 Key Learning Objectives  
- Understand neurons, layers, activations, and forward propagation  
- Implement a neural network manually using **NumPy**  
- Build and train models using **PyTorch** and **TensorFlow/Keras**  
- Compare training loops, optimizers, and workflows  
- Perform hyperparameter tuning  
- Apply dropout to reduce overfitting  
- Visualize performance and evaluate results  

---

## 🔹 Part 1 — Neural Network From Scratch (NumPy)  
### **What I Built:**  
- Manual implementation of:  
  - Forward pass  
  - Activation functions (ReLU, Softmax)  
  - Loss calculation  
  - Weight updates  
- Trained a simple classifier on Fashion‑MNIST‑like data  

### **Key Takeaways:**  
- Learned how gradients flow through layers  
- Understood how weights and biases update  
- Saw how training works without any frameworks  

---

## 🔹 Part 2 — PyTorch Implementation  
### **Model Architecture:**  
- Flatten → Dense(512) → ReLU  
- Dense(512) → ReLU  
- Dense(10) output layer  

### **What I Learned:**  
- How to define models using `nn.Module`  
- How to write a full training loop:  
  - `optimizer.zero_grad()`  
  - `loss.backward()`  
  - `optimizer.step()`  
- How to evaluate using validation accuracy  

### **Results:**  
- Achieved ~88–89% validation accuracy  
- Understood the flexibility and debugging advantages of PyTorch  

---

## 🔹 Part 3 — TensorFlow/Keras Implementation  
### **Model Architecture:**  
- Flatten → Dense(512, ReLU)  
- Dense(512, ReLU)  
- Dense(10)  

### **What I Learned:**  
- Keras simplifies training using `model.compile()` and `model.fit()`  
- No need to manually write training loops  
- Easy to monitor accuracy and loss  

### **Results:**  
- Achieved ~91–92% accuracy  
- Faster experimentation due to high‑level API  

---

## 🔹 Part 4 — Hyperparameter Tuning  
### **Experiments:**  
- Learning rates: 0.01 vs 0.0001  
- Epochs: 5 vs 15  
- Batch sizes: 64 vs 128  

### **Findings:**  
- Lower learning rate + more epochs improved stability  
- Larger batch size smoothed gradient updates  
- Validation accuracy improved by ~2–3%  

---

## 🔹 Part 5 — Dropout to Reduce Overfitting  
### **Added:**  
- `nn.Dropout(0.5)` in PyTorch model  

### **Impact:**  
- Reduced overfitting  
- Validation accuracy became more stable  
- Training accuracy decreased slightly (expected)  

---

## 🔹 Final Improved Model  
### **Architecture Changes:**  
- Added extra hidden layer  
- Used LeakyReLU  
- Increased dropout to 0.3  

### **Results:**  
- Validation accuracy improved to ~88.6%  
- More stable loss curve  
- Better generalization  

---

## 🔹 Reflection  
This module helped me understand neural networks at every level — from raw matrix math to high‑level frameworks.  
By building models manually and then recreating them in PyTorch and Keras, I gained a deeper understanding of:  
- How training loops work  
- How gradients update weights  
- Why frameworks automate certain steps  
- How hyperparameters affect performance  

This foundation prepared me for more advanced deep learning topics such as CNNs, RNNs, Transformers, and Reinforcement Learning.

---

## 📁 Files Included  
- `numpy_nn.ipynb` — Neural network from scratch  
- `pytorch_model.ipynb` — PyTorch implementation  
- `keras_model.ipynb` — TensorFlow/Keras implementation  
- `improved_model.ipynb` — Hyperparameter tuning + dropout  
- Training logs, accuracy charts, and confusion matrices  


