# 🎨 A Comparative Study of Pretrained Models and Optimized EfficientNet for Art Movement Classification

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![PyTorch](https://img.shields.io/badge/Framework-PyTorch-red.svg)
![CUDA](https://img.shields.io/badge/Accelerated-CUDA-green.svg)
![Status](https://img.shields.io/badge/Status-Research%20Study-yellow.svg)

---

## 📌 Overview

This repository presents a research-oriented comparative study of pretrained deep convolutional neural networks for **fine-grained art movement classification**.

The study evaluates multiple pretrained architectures under a controlled experimental framework and further optimizes **EfficientNet-B7** through principled fine-tuning and regularization techniques.

### Research Objectives

- Analyze model scaling behavior across EfficientNet variants  
- Study representation capacity vs generalization trade-offs  
- Evaluate transfer learning strategies for stylistic visual classification  
- Measure performance gains through targeted optimization  

---

## 🧠 Problem Context

Art movement classification is a challenging computer vision task due to:

- High intra-class variability  
- Strong stylistic similarity across classes  
- Texture- and pattern-driven visual semantics  
- Subtle compositional differences between movements  

Unlike object recognition tasks, stylistic classification requires models to capture fine-grained visual cues such as brush strokes, color palettes, and structural abstractions.

This project investigates how pretrained CNN architectures perform under these constraints and how structured optimization impacts generalization performance.

---

## 🏗️ Methodology

### 🔬 Comparative Architecture Study

Pretrained ImageNet models evaluated:

- ResNet50  
- DenseNet121  
- EfficientNet-B0  
- EfficientNet-B1  
- EfficientNet-B2  
- EfficientNet-B3  
- EfficientNet-B4  
- EfficientNet-B5  
- EfficientNet-B6  
- EfficientNet-B7  

### Common Experimental Setup

- 80/20 train-validation split  
- Fixed random seed for reproducibility  
- Input resolution: 224 × 224  
- Loss Function: CrossEntropyLoss  
- GPU-accelerated training (CUDA)

### Evaluation Metrics

- Training accuracy curves  
- Validation accuracy curves  
- Training loss curves  
- Validation loss curves  
- Normalized confusion matrices  

---

## 🚀 EfficientNet-B7 Baseline Configuration

- ImageNet-initialized backbone  
- Feature extractor frozen  
- Classifier retrained for 11 art movement classes  
- Optimizer: Adam  
- Learning rate: 1e-3  
- Early stopping (patience = 5)  
- Maximum epochs: 100  

### Baseline Performance

- Validation Accuracy: ~64%

---

## ⚡ EfficientNet-B7 Optimization Strategy

To improve generalization performance, the following refinements were applied:

- Selective layer unfreezing (partial fine-tuning)
- Optimizer switched to AdamW
- Reduced learning rate
- Weight decay regularization
- Early stopping retained

### Optimized Performance

- Validation Accuracy: ~74%

This represents an approximate **10% absolute improvement** over the baseline configuration.

---

## 📊 Key Findings

- EfficientNet scaling improves representational capacity for fine-grained stylistic tasks.
- Larger EfficientNet variants demonstrate better generalization when properly fine-tuned.
- EfficientNet-B7 outperformed ResNet50 and DenseNet121 in this experimental setup.
- Targeted optimization significantly reduced inter-class confusion among visually similar movements.
- Transfer learning combined with selective fine-tuning yields strong performance gains.

---

## 📈 Performance Insights

- Smaller EfficientNet variants train faster but exhibit lower representational depth.
- Fully frozen backbones underperform in stylistic classification tasks.
- Fine-tuning deeper layers improves discrimination between visually similar art movements.
- Regularization (weight decay + learning rate reduction) enhances stability and reduces overfitting.

---

## ⚙️ Tech Stack

### Programming Language
- Python

### Deep Learning Framework
- PyTorch

### Hardware Acceleration
- CUDA

### Supporting Libraries
- NumPy
- Matplotlib
- Scikit-learn

---

## 🔬 Research Contributions

- Systematic evaluation of EfficientNet scaling for stylistic classification
- Empirical validation of optimization strategies in fine-grained visual domains
- Demonstration of performance scaling through principled fine-tuning
- Benchmark comparison across major pretrained CNN architectures

---

## 🌍 Applications

Fine-grained art movement classification can support:

- Digital art archiving systems  
- Museum catalog automation  
- Art authentication research  
- Educational visualization tools  
- Computational art history studies  

---

## 📬 Contact

For research discussions, academic collaboration, or technical inquiries, feel free to connect.
