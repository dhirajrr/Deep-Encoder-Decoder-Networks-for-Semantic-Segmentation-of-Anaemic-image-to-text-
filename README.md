Here's a professional and comprehensive `README.md` for your GitHub repository based on your project poster and LinkedIn content:

---

# 🔬 Deep Encoder-Decoder Networks for Semantic Segmentation of Anaemic RBCs and Image Captioning

## 📌 Project Overview

This project explores deep learning-based encoder-decoder architectures to solve two key tasks:

1. **Semantic segmentation** of anaemic Red Blood Cells (RBCs)
2. **Medical image captioning** (image-to-text generation)

We implemented and compared three models:

* **Baseline LSTM without Attention**
* **Bahdanau Attention-based RNN**
* **Transformer (Self-Attention)**

Each model was evaluated on medical imaging data using popular NLP metrics (BLEU, ROUGE, METEOR, SPICE) to assess caption quality and diagnostic relevance.

---

## 🎯 Objectives

* Implement deep encoder-decoder models with varying attention mechanisms
* Train on a real-world RBC CELL dataset (microscopic images of anaemic vs. normal cells)
* Generate medical captions and compare model performance

---

## 🧠 Model Architectures

* 🔹 **LSTM (No Attention):** Uses fixed context from the last encoder state
* 🔹 **GRU with Bahdanau Attention:** Dynamically attends to relevant encoder outputs
* 🔹 **Transformer (Self-Attention):** Learns dependencies across the input using positional encoding and multi-head attention

All models are built using **TensorFlow/Keras** and trained on padded article-headline pairs.

---

## 📁 Dataset Description

* **Type:** Microscopic images of Red Blood Cells (RBCs)
* **Format:** `.jpg` images
* **Classes:** `Anaemia`, `Normal`
* **Labels:** Inferred from folder names
* **Usage:** Binary classification & sequence-to-sequence medical caption generation

---

## 📊 Evaluation Metrics

| Metric | Score         |
| ------ | ------------- |
| BLEU   | 1.82 × 10⁻²³¹ |
| METEOR | 0.5           |
| SPICE  | 1.0           |

We also visualized:

* **Training Time Comparison**
* **BLEU & ROUGE Score Comparison**
* **Attention Mechanism Flowcharts**

---

## 📉 Results & Insights

* ✅ Transformer model gave **best BLEU and ROUGE** scores.
* 🎯 Attention-based models provided better contextual relevance in captions.
* 🧠 Demonstrated how attention improves performance in NLP + vision fusion tasks.

---

## 🔧 Working Principle

* **No Attention:** Relies solely on the final encoder output.
* **Bahdanau Attention:** Dynamically computes attention weights over encoder states.
* **Self-Attention (Transformer):** Utilizes multi-head attention to capture long-range dependencies.

---

## 📄 Reference

Based on the paper:
**"Semantic Segmentation of Anaemic RBCs Using Multilevel Deep Convolutional Encoder-Decoder Network"**
M. Shahzad, A. I. Umar, S. H. Shirazi, and I. A. Shaikh
📚 *IEEE Access*, vol. 9, pp. 161326–161341, 2021
🔗 [DOI: 10.1109/ACCESS.2021.3113768](https://doi.org/10.1109/ACCESS.2021.3113768)

---

## 🧑‍💻 Authors

* Dhiraj Rathod
* Sanke Nane
* Komal Katare
  **Mentor:** Prof. Diptee Chikmurge
  📍 MIT Academy of Engineering, Pune




## 🚀 How to Run

```bash
git clone https://github.com/your-username/rbc-captioning-transformer.git
cd rbc-captioning-transformer

# Create virtual environment
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

# Run training
python train_model.py --model transformer

# Evaluate and generate captions
python evaluate_model.py --input test_images/
```

---

## 🗂️ Folder Structure

```
├── data/
│   ├── anaemic/
│   ├── normal/
├── models/
│   ├── lstm_model.py
│   ├── attention_model.py
│   └── transformer_model.py
├── utils/
│   └── preprocessing.py
├── assets/
│   └── project_poster.png
├── train_model.py
├── evaluate_model.py
└── README.md
```

---
