# Emotion Classification using LSTM in PyTorch

## Overview

This project implements a deep learning based **Text Emotion Classification System** using **PyTorch** and **LSTM (Long Short-Term Memory)** networks.

The model is trained on the **DAIR-AI Emotion Dataset** and classifies text into six different emotion categories:

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
- Model training and evaluation
- Emotion inference on custom text

---

# Features

- Complete NLP preprocessing pipeline built manually
- Custom vocabulary generation
- Integer sequence encoding
- Sequence padding and truncation
- PyTorch Dataset and DataLoader implementation
- LSTM based text classification model
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
LSTM Network
   ↓
Fully Connected Layer
   ↓
Emotion Prediction
```

---

# Model Architecture

The model architecture consists of:

1. Embedding Layer
2. LSTM Layer
3. Fully Connected Classification Layer

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

## Final Results

| Metric | Score |
|---|---|
| Training Accuracy | 98.94% |
| Validation Accuracy | 86.70% |
| Test Accuracy | 85.90% |

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

A confusion matrix is generated to visualize:
- Correct predictions
- Misclassified emotions
- Emotion-wise model performance

---

# Classification Report

The project includes a detailed classification report containing:
- Precision
- Recall
- F1-score
- Support

for each emotion category.

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
git clone (https://github.com/Hari-jith/Natural-Language-Processing/Emotion-Classification-LSTM)
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
text_emotion_detection.ipynb
```

Run all notebook cells sequentially.

---

# Future Improvements

Possible future enhancements:

- Bidirectional LSTM (BiLSTM)
- Dropout Regularization
- Attention Mechanism
- GloVe Word Embeddings
- GRU Architecture
- Hyperparameter Tuning
- Streamlit Web App Deployment
- Transformer-based Comparison
- Real-time Emotion Detection API

---

# Learning Outcomes

This project demonstrates understanding of:

- Fundamental NLP concepts
- Sequence modeling
- Deep learning for text classification
- PyTorch workflow
- Recurrent neural networks
- LSTM architecture
- Model training and evaluation
- NLP preprocessing pipeline design

---

# Conclusion

This project successfully demonstrates how deep learning and NLP techniques can be combined to build an effective emotion classification system using PyTorch and LSTM networks without relying on transformer architectures.

The model achieved strong classification performance while maintaining a fully explainable and educational NLP pipeline.

---

# Author

## Harijith M M

---
