# 📘 Lab 05 — RNNs vs Transformers vs Vision Transformers  
**Course:** ITAI 2376 — Deep Learning  
**Student:** Aima Ayaz  
**Date:** Spring 2026  

---

## 🔹 Overview  
This lab compares three major deep learning architectures across text and image tasks:

1. **RNNs (LSTM, GRU, Vanilla RNN)** — sequence‑based models  
2. **Transformers (DistilBERT)** — attention‑based NLP model  
3. **Vision Transformer (ViT)** — transformer architecture applied to images  

The goal was to understand how each architecture processes data, how they differ in performance, and why modern AI systems increasingly rely on transformer‑based models.

---

## 🔹 Part A — RNN Text Classification (AG News)  

### **Task:**  
Classify news articles into 4 categories:  
- World  
- Sports  
- Business  
- Sci/Tech  

### **Models Implemented:**  
- **LSTM (Bidirectional)**  
- **GRU (Bidirectional)**  
- **Vanilla RNN**  

### **Pipeline:**  
- Custom tokenization  
- Vocabulary building (10,000 words)  
- Sequence padding (128 tokens)  
- PyTorch Dataset + DataLoader  
- Training + evaluation loops  

### **Results:**  
| Model | Test Accuracy | Notes |
|-------|--------------|-------|
| **Vanilla RNN** | ~0.74 | Fastest but weakest (vanishing gradients) |
| **LSTM** | ~0.79 | Strong long‑term memory |
| **GRU** | ~0.81 | Best performance + fewer parameters |

### **Key Takeaways:**  
- Gated architectures (LSTM/GRU) outperform vanilla RNNs  
- GRU is more efficient while maintaining high accuracy  
- RNNs struggle with long‑range dependencies  

---

## 🔹 Part B — Transformer Text Classification (DistilBERT)  

### **Task:**  
Use **DistilBERT** to classify AG News articles (same dataset as RNNs).

### **Why Transformers?**  
- Use **self‑attention** instead of recurrence  
- Capture long‑range dependencies easily  
- Pretrained on massive corpora → strong out‑of‑the‑box performance  

### **Pipeline:**  
- Hugging Face `datasets` + `transformers`  
- Tokenization with BERT tokenizer  
- Fine‑tuning DistilBERT classifier  

### **Results:**  
- Significantly higher accuracy than RNNs  
- Faster convergence  
- Better generalization  

### **Key Takeaways:**  
Transformers outperform RNNs because they:  
- Process sequences in parallel  
- Capture global context  
- Use pretrained knowledge  

---

## 🔹 Part C — Vision Transformer (ViT) on CIFAR‑10  

### **Task:**  
Classify CIFAR‑10 images (10 classes) using a **Vision Transformer**.

### **Why ViT?**  
- Applies transformer attention to image patches  
- Competes with CNNs on vision tasks  
- Learns global relationships between patches  

### **Pipeline:**  
- Load CIFAR‑10  
- Preprocess images into patches  
- Fine‑tune ViT model  

### **Results:**  
- Strong performance despite small dataset  
- Demonstrates transformer versatility beyond text  

---

## 🔹 Part D — Comparative Analysis  

### **Text Models:**  
| Architecture | Strengths | Weaknesses |
|--------------|-----------|------------|
| **Vanilla RNN** | Simple, fast | Poor long‑term memory |
| **LSTM** | Great for long sequences | More parameters |
| **GRU** | Efficient + strong performance | Slightly less expressive than LSTM |
| **DistilBERT** | Best accuracy, pretrained, parallelizable | Requires more compute |

### **Image Models:**  
| Architecture | Strengths | Weaknesses |
|--------------|-----------|------------|
| **CNN** | Excellent local feature extraction | Limited global context |
| **ViT** | Global attention, scalable | Needs large data or pretraining |

---

## 🔹 Key Learnings  
- Transformers outperform RNNs on text tasks due to attention and parallelism  
- GRU is a strong balance of speed and accuracy  
- ViT shows that transformer architectures generalize beyond NLP  
- Pretrained models dramatically improve performance  
- Modern AI systems rely heavily on transformer‑based architectures  

---

## 📁 Files Included  
- `L05_Aima_Ayaz_ITAI2376.ipynb` — Full lab notebook  
- Tokenization, vocabulary, and preprocessing scripts  
- RNN, LSTM, GRU model implementations  
- DistilBERT fine‑tuning code  
- ViT training and evaluation  


