# Emotion Classification using LSTM and BiLSTM in PyTorch

## Overview

This project implements a deep learning based **Text Emotion Classification System** using **PyTorch**, **LSTM (Long Short-Term Memory)**, and **Bidirectional LSTM (BiLSTM)** networks.

The models are trained on the **DAIR-AI Emotion Dataset** and classify text into six different emotion categories:

- Sadness
- Joy
- Love
- Anger
- Fear
- Surprise

Unlike modern transformer-based approaches, this project focuses on building a complete NLP pipeline from scratch using foundational Natural Language Processing concepts and recurrent neural networks.

The project covers:
- Text preprocessing
- Tokenization
- Vocabulary building
- Sequence encoding
- Padding and truncation
- Custom PyTorch Dataset and DataLoader
- Embedding layers
- LSTM architecture
- BiLSTM architecture
- Model training and evaluation
- Comparative model analysis
- Emotion inference on custom text

---

# Features

- Complete NLP preprocessing pipeline built manually
- Custom vocabulary generation
- Integer sequence encoding
- Sequence padding and truncation
- PyTorch Dataset and DataLoader implementation
- LSTM based text classification model
- BiLSTM based text classification model
- Comparative performance evaluation
- Training and validation pipeline
- Accuracy and loss visualization
- Confusion matrix visualization
- Classification report generation
- Custom emotion prediction inference
- Model saving and loading support

---

# Technologies Used

- Python
- PyTorch
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Hugging Face Datasets
- Jupyter Notebook

---

# Dataset

Dataset used:

## DAIR-AI Emotion Dataset

Dataset Link:

https://huggingface.co/datasets/dair-ai/emotion

The dataset contains:
- 16,000 training samples
- 2,000 validation samples
- 2,000 test samples

---

# Emotion Classes

| Label ID | Emotion |
|---|---|
| 0 | sadness |
| 1 | joy |
| 2 | love |
| 3 | anger |
| 4 | fear |
| 5 | surprise |

---

# Project Workflow

```text
Raw Text
   ↓
Text Cleaning
   ↓
Tokenization
   ↓
Vocabulary Building
   ↓
Word-to-Index Mapping
   ↓
Integer Encoding
   ↓
Padding & Truncation
   ↓
PyTorch Dataset & DataLoader
   ↓
Embedding Layer
   ↓
LSTM / BiLSTM Network
   ↓
Fully Connected Layer
   ↓
Emotion Prediction
```

---

# Model Architectures

The project implements two deep learning architectures:

## 1. LSTM Model

A standard Long Short-Term Memory network that processes text sequences from left to right.

### Architecture Flow

```text
Input Text
    ↓
Embedding Layer
    ↓
LSTM Network
    ↓
Hidden Representation
    ↓
Fully Connected Layer
    ↓
Emotion Prediction
```

---

## 2. Bidirectional LSTM (BiLSTM)

A Bidirectional LSTM processes text sequences in both directions:
- Left → Right
- Right → Left

This improves contextual understanding and sequence learning.

### BiLSTM Architecture Flow

```text
Input Text
    ↓
Embedding Layer
    ↓
Forward LSTM
    ↓
Backward LSTM
    ↓
Concatenated Hidden States
    ↓
Fully Connected Layer
    ↓
Emotion Prediction
```

---

# NLP Preprocessing Steps

The following preprocessing techniques were implemented manually:

- Lowercasing text
- Removing special characters
- Tokenization
- Vocabulary creation
- Word frequency analysis
- Integer sequence conversion
- Padding and truncation

---

# Hyperparameters

| Hyperparameter | Value |
|---|---|
| Embedding Dimension | 128 |
| Hidden Dimension | 256 |
| Batch Size | 32 |
| Learning Rate | 0.001 |
| Maximum Sequence Length | 25 |
| Number of Epochs | 10 |
| Optimizer | Adam |
| Loss Function | CrossEntropyLoss |

---

# Model Performance

## Final Model Comparison

| Model | Test Accuracy | Test Loss |
|---|---|---|
| LSTM | 85.90% | 0.6047 |
| BiLSTM | 86.65% | 0.5403 |

The BiLSTM model achieved better contextual understanding and improved overall classification performance compared to the standard LSTM model.

---

# BiLSTM Classification Report

| Emotion | Precision | Recall | F1-Score |
|---|---|---|---|
| sadness | 0.91 | 0.92 | 0.91 |
| joy | 0.89 | 0.88 | 0.89 |
| love | 0.73 | 0.73 | 0.73 |
| anger | 0.85 | 0.85 | 0.85 |
| fear | 0.85 | 0.85 | 0.85 |
| surprise | 0.67 | 0.73 | 0.70 |

Overall Accuracy: **86.65%**

---

# Training Curves

The project includes:
- Training vs Validation Loss Graph
- Training vs Validation Accuracy Graph

These visualizations help analyze:
- Model learning behavior
- Convergence
- Overfitting trends

---

# Confusion Matrix

Confusion matrices are generated for both:
- LSTM
- BiLSTM

These visualizations help analyze:
- Correct predictions
- Misclassified emotions
- Emotion-wise model performance

---

# Sample Predictions

| Input Text | Predicted Emotion |
|---|---|
| I am feeling very happy today | joy |
| I am scared about the exam | fear |
| I miss my friends and feel lonely | sadness |

---

# Installation

## Clone Repository

```bash
git clone https://github.com/Hari-jith/Natural-Language-Processing.git
```

---

## Navigate to Project Folder

```bash
cd Natural-Language-Processing
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
Text_Emotion_Detection_Comparative_Model.ipynb
```

Run all notebook cells sequentially.

---

# Future Improvements

Possible future enhancements:

- Attention Mechanism
- GloVe Word Embeddings
- GRU Architecture
- Hyperparameter Tuning
- Streamlit Web App Deployment
- Transformer-based Comparison
- Real-time Emotion Detection API
- BERT-based Emotion Classification

---

# Learning Outcomes

This project demonstrates understanding of:

- Fundamental NLP concepts
- Sequence modeling
- Deep learning for text classification
- PyTorch workflow
- Recurrent neural networks
- LSTM architecture
- Bidirectional LSTM architecture
- Model comparison and evaluation
- NLP preprocessing pipeline design

---

# Conclusion

This project successfully demonstrates how deep learning and NLP techniques can be combined to build effective emotion classification systems using PyTorch and recurrent neural networks.

Both LSTM and BiLSTM architectures were implemented and evaluated on the DAIR-AI Emotion Dataset. The BiLSTM model achieved improved performance by learning contextual information from both forward and backward directions in text sequences.

The project achieved strong classification performance while maintaining a fully explainable and educational NLP pipeline without relying on transformer-based architectures.

---

# Author

## Harijith M M
