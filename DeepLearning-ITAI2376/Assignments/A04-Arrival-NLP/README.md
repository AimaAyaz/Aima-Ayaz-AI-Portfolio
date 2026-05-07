# 📄 A04 — Analyzing *Arrival* Through the Lens of NLP  
**Course:** ITAI 2376 — Deep Learning  
**Authors:** Group 8 — Aima Ayaz & Nicole Marcial  
**Date:** February 12, 2026  

---

## 🔹 Overview  
This assignment analyzes the film *Arrival* using concepts from Natural Language Processing (NLP).  
The movie centers on communication rather than invasion, making it a powerful metaphor for the challenges of language understanding, translation, ambiguity, and context — all core problems in NLP.

---

## 🔹 Key NLP Connections in the Film  

### **1. Machine Translation & Context Sensitivity**  
- The phrase **“offer weapon”** triggers global panic due to misinterpretation.  
- Similar to real NLP systems, meaning depends heavily on **context**, domain, and intent.  
- Models trained on general corpora often struggle in specialized domains (military, medical, legal).

---

### **2. Text Preprocessing & Tokenization**  
Dr. Louise performs manual versions of preprocessing steps:  
- Cleaning and isolating alien symbols  
- Breaking complex circular logograms into smaller units  
- Identifying repeated patterns  

This mirrors:  
- Tokenization  
- Normalization  
- Feature extraction  

---

### **3. Building a Corpus & TF‑IDF‑like Reasoning**  
As more alien messages are collected, Louise builds a **corpus**.  
She tracks:  
- Frequently appearing symbols  
- Rare symbols  
- Context‑specific patterns  

This resembles **TF‑IDF**, where important terms are identified by frequency and relevance.

---

### **4. Ambiguity & Word Sense Disambiguation**  
Words like *bank* (riverbank vs. financial institution) show how meaning shifts with context.  
In the film:  
- “Offer weapon” could mean a literal weapon or a tool.  
- Without context, both humans and machines default to the most threatening interpretation.  

Modern NLP solves this using **contextual embeddings** (e.g., BERT).

---

### **5. Syntax, Structure & Dependency Parsing**  
Understanding grammatical relationships is essential.  
Governments interpret the phrase literally, while Louise analyzes deeper structure and intent.  
This parallels:  
- Part‑of‑speech tagging  
- Dependency parsing  
- Semantic role labeling  

---

### **6. Sentiment Analysis Limitations**  
A sentiment model would classify “offer weapon” as negative.  
But the aliens’ intent may not be hostile.  
This shows how sentiment models can misclassify text without domain adaptation.

---

### **7. Named Entity Recognition (NER)**  
When Louise labels “HUMAN” and points to herself, she is mapping symbols to entities.  
This resembles **supervised learning** and **NER**, where models learn to associate tokens with real‑world concepts.

---

### **8. Multi‑Class Classification Across Nations**  
Each country interprets the alien message differently:  
- Threat  
- Cooperation  
- Warning  
- Uncertainty  

This mirrors how different models (or datasets) can produce different classifications based on assumptions and training.

---

### **9. Non‑Linear Language Structure**  
The alien writing system is **circular** and **semasiographic** — conveying meaning directly rather than representing sound.  
This challenges linear NLP models and highlights the diversity of real‑world communication systems.

---

## 🔹 Conclusion  
*Arrival* illustrates many of the same challenges studied in NLP:  
- Ambiguity  
- Context dependence  
- Translation errors  
- Feature extraction  
- Corpus building  
- Entity mapping  

The film shows that true understanding requires more than decoding symbols — it requires interpreting **intent, structure, and context**, just like modern NLP systems.

---

## 🔹 Sources  
- ITAI 2373 Modules 1–13 PowerPoints  
- *Arrival* (2016), directed by Denis Villeneuve  

