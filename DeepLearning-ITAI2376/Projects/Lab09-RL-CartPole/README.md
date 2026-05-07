# 📘 Module 09 — Reinforcement Learning Foundations: CartPole Agent  
**Course:** ITAI 2376 — Deep Learning  
**Student:** Aima Ayaz  
**Date:** Spring 2026  

---

## 🔹 Overview  
This project introduces **Reinforcement Learning (RL)** through the classic **CartPole‑v1** environment.  
The goal was to understand the RL loop — **state → action → reward → next state** — and observe how an agent improves over time through trial and error.

You implemented and compared:  
- A **Random Agent** (baseline)  
- A **Q‑Learning Agent** (tabular RL)  
- Exploration vs exploitation experiments (epsilon decay)  
- Learning curve visualizations  

This module builds intuition for RL concepts used in modern systems, including RLHF (Reinforcement Learning from Human Feedback).

---

## 🔹 Environment: CartPole‑v1  
The agent must balance a pole on a moving cart by choosing actions:  
- **0 = push left**  
- **1 = push right**

### **State Variables:**  
1. Cart position  
2. Cart velocity  
3. Pole angle  
4. Pole angular velocity  

### **Reward:**  
+1 for every timestep the pole stays upright  
(Max score = 500)

---

## 🔹 Part 1 — Random Agent (Baseline)  
### **Behavior:**  
- Takes random actions with no strategy  
- Fails quickly (pole falls within ~10–30 steps)

### **Results:**  
- Average score: ~20  
- Demonstrates why learning is necessary  

### **Key Insight:**  
You cannot appreciate learning until you see what *no learning* looks like.

---

## 🔹 Part 2 — Q‑Learning Agent  
### **Why Q‑Learning?**  
- Simple but powerful RL algorithm  
- Learns a table of action values (Q‑table)  
- Updates values based on reward + future reward estimates  

### **Challenges:**  
CartPole has continuous state variables → must be **discretized** into bins.

### **Q‑Learning Update Rule:**  
Q(s, a) ← Q(s, a) + α [ reward + γ max(Q(s'), a') − Q(s, a) ]

---

### **Training Setup:**  
- Episodes: 500  
- Learning rate: 0.1  
- Discount factor: 0.99  
- Epsilon‑greedy exploration  
- Epsilon decay: 0.995 → 0.01  

### **Results:**  
- Early episodes: unstable, low scores  
- Later episodes: stable improvement  
- Final 50‑episode average: ~90  
- Clear upward learning curve  

### **Key Insight:**  
The agent learns to keep the pole balanced longer by updating its Q‑table based on experience.

---

## 🔹 Part 3 — Exploration vs Exploitation  
You trained two additional agents:

### **Agent A — Fast Decay (ε = 0.990)**  
- Explores less  
- Learns faster early  
- Plateaus earlier  

### **Agent B — Slow Decay (ε = 0.999)**  
- Explores more  
- Slower early learning  
- Better long‑term performance  

### **Original (ε = 0.995)**  
- Balanced performance  

### **Takeaway:**  
Exploration is essential — decaying epsilon too quickly can trap the agent in suboptimal behavior.

---

## 🔹 Visualizations  
You plotted:

### **1. Learning Curve**  
- Blue: raw episode scores  
- Orange: rolling average (50 episodes)  
- Shows clear improvement over time  

### **2. Epsilon Decay Curve**  
- High exploration early  
- Low exploration later  
- Demonstrates shift from exploring → exploiting  

---

## 🔹 Reflection  
This module provided hands‑on experience with the core ideas behind reinforcement learning:

- Agents learn through **trial and error**  
- Rewards shape behavior  
- Exploration is necessary for discovering better strategies  
- Even simple RL algorithms can learn surprisingly effective policies  
- RL concepts connect directly to **RLHF**, used in training modern LLMs  

By watching the agent improve from random flailing to stable balancing, you gained intuition for how RL systems learn and adapt.

---

## 📁 Files Included  
- `L09_Aima_Ayaz_ITAI2376.ipynb` — Full RL notebook  
- Random agent implementation  
- Q‑Learning agent with discretization  
- Exploration decay experiments  
- Learning curve + epsilon decay plots  


