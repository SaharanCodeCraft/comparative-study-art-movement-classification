# 🎨 A Comparative Study of Pretrained Models and Optimized EfficientNet for Art Movement Classification

## 📌 Overview

This repository presents a research-oriented comparative study of pretrained deep convolutional neural networks for fine-grained art movement classification.

The study evaluates multiple pretrained architectures (ResNet50, DenseNet121, EfficientNet B0–B7) under a controlled experimental setup and further optimizes EfficientNet-B7 through principled fine-tuning and regularization techniques.

The objective is to analyze:

- Model scaling behavior across EfficientNet variants  
- Representation capacity vs generalization trade-offs  
- Transfer learning strategies for stylistic visual classification  
- Performance gains through targeted optimization  

---

## 🧠 Problem Context

Art movement classification is a challenging computer vision task due to:

- High intra-class variability  
- Strong stylistic similarity across classes  
- Texture- and pattern-driven visual semantics  

This project investigates how pretrained CNN architectures perform under these fine-grained visual constraints and how optimization strategies impact generalization performance.

---

## 🏗️ Methodology

### Comparative Architecture Study

Pretrained ImageNet models evaluated:

- ResNet50  
- DenseNet121  
- EfficientNet-B0 → B7  

Common experimental setup:

- 80/20 train-validation split  
- Fixed random seed for reproducibility  
- Input resolution: 224 × 224  
- Light data augmentation (resize, horizontal flip, normalization)  
- CrossEntropy loss  
- GPU-accelerated training (CUDA)

Performance evaluation included:

- Training and validation accuracy curves  
- Training and validation loss curves  
- Normalized confusion matrices  

---

### EfficientNet-B7 Baseline

- ImageNet-initialized backbone  
- Feature extractor frozen  
- Classifier retrained for 11 classes  
- Optimizer: Adam (learning rate = 1e-3)  
- Early stopping (patience = 5)  
- Maximum epochs: 100  

Baseline validation accuracy: **~64%**

---

### EfficientNet-B7 Optimization

To improve generalization:

- Selective layer unfreezing  
- Optimizer switched to AdamW  
- Reduced learning rate  
- Weight decay regularization  
- Early stopping applied  

Optimized validation accuracy: **~74%**

This represents an approximate **10% absolute improvement** over the baseline configuration.

---

## 📊 Key Findings

- EfficientNet scaling demonstrates improved representational capacity for fine-grained stylistic classification tasks.  
- EfficientNet-B7 outperformed other evaluated architectures when appropriately fine-tuned.  
- Targeted optimization significantly reduced inter-class confusion among visually similar art movements.

---

## ⚙️ Tech Stack

- Python  
- PyTorch  
- CUDA  
- NumPy  
- Matplotlib  
- Scikit-learn  

---

## 📬 Contact

For research discussions or collaboration opportunities, feel free to connect.
