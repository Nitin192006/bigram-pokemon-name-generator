# 🧠 Pokémon Name Generator
![Python](https://img.shields.io/badge/Python-3.x-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626)
![Bigram](https://img.shields.io/badge/Model-Bigram-purple)
![Count Matrix](https://img.shields.io/badge/Count%20Model-Bigram%20Counts-orange)
![Neural Bigram](https://img.shields.io/badge/Neural%20Model-Single%20Layer%20NN-darkgreen)
![Generative AI](https://img.shields.io/badge/Task-Name%20Generation-success)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

A character-level language model built from scratch in PyTorch that learns how Pokémon names are formed and generates entirely new names one character at a time.

Inspired by Andrej Karpathy's *Neural Networks: Zero to Hero* series.

---

## 🚀 Overview

This project explores the foundations of language modeling by implementing two approaches:

### 1️⃣ Count-Based Bigram Model
Uses character transition frequencies directly from the dataset.

### 2️⃣ Neural Network Bigram Model
Learns character transition probabilities using:

- One-Hot Encoding
- Matrix Multiplication
- Softmax
- Negative Log-Likelihood Loss
- Gradient Descent

The neural network learns nearly the same probability distribution as the count-based model.

---

## 🏗️ Model Pipeline

```text
Current Character
        │
        ▼
 One-Hot Encoding
        │
        ▼
   Weight Matrix
      (27×27)
        │
        ▼
      Logits
        │
        ▼
     Softmax
        │
        ▼
 Next Character
```

---

## 📊 Bigram Learning

The model learns probabilities such as:

```text
P(next='i' | current='p')
P(next='a' | current='k')
P(next='r' | current='a')
```

These learned character transitions allow the model to generate realistic Pokémon-like names.

---

## ⚡ Name Generation Process

```text
START
  │
  ▼
  p
  ▼
  i
  ▼
  k
  ▼
  a
  ▼
  r
  ▼
  u
  ▼
 END
```

At each step, the next character is sampled from the learned probability distribution.

---

## 🧩 Concepts Implemented

- Character-Level Language Models
- Bigram Probability Estimation
- One-Hot Encoding
- Matrix Multiplication
- Softmax
- Log Likelihood
- Negative Log-Likelihood Loss
- Gradient Descent
- Backpropagation
- Sampling from Probability Distributions
- PyTorch Tensor Operations

---

## 🛠️ Tech Stack

| Tool | Purpose |
|--------|--------|
| Python | Core Programming |
| PyTorch | Neural Network Implementation |
| NumPy | Numerical Operations |
| Matplotlib | Visualizations |
| Jupyter Notebook | Development Environment |

---

## 📁 Repository Structure

```text
pokemon-name-generator/
│
├── pokemon_name_generator.ipynb
├── names.txt
└── README.md
```

---

## ▶️ Running the Project

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/pokemon-name-generator.git
cd pokemon-name-generator
```

Launch Jupyter Notebook:

```bash
jupyter notebook pokemon_name_generator.ipynb
```

Run all notebook cells sequentially.

---

## 🎯 Key Takeaway

This project demonstrates how a simple single-layer neural network can learn the same character-transition statistics as a traditional count-based bigram model.

It serves as an introduction to:

- Language Modeling
- Neural Networks
- Probability Distributions
- Gradient-Based Learning

---

## 🙏 Acknowledgements

Inspired by Andrej Karpathy's **Neural Networks: Zero to Hero** series and the **makemore** project.
