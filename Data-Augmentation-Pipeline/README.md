# Low-Resource Fake News Detection: Synthetic Data Augmentation & Transformer Pipeline 🧪📉

An end-to-end, data-centric NLP engineering pipeline designed to combat the "Cold Start" data scarcity crisis in text classification. In production environments (such as real-time misinformation monitoring or rumor tracking), malicious actors shift narratives rapidly. Consequently, machine learning models often catch only a handful of seed examples before needing to deploy a defense. Training directly on such skewed data leads to extreme overfitting or severe majority-class bias.

This repository implements a two-stage Transformer architecture to solve this challenge. **Stage 1** utilizes a generative sequence-to-sequence LLM (`Flan-T5-Base`) to perform stylized, feature-guided text expansions on an extremely scarce minority class. **Stage 2** takes the freshly balanced data matrix and fine-tunes an encoder-based Transformer (`DistilBERT-Base-Uncased`) with a sequence classification head, achieving exceptional downstream precision and recall.

---

## 🚀 Architectural Blueprint

The lifecycle of this repository shifts focus from standard model tuning to robust data curation, optimization, and evaluation:

1. **Unstructured Data Ingestion:** Dynamic fetching of real-world text streams using the academic `20Newsgroups` library.
2. **Induced Structural Scarcity:** Extreme downsampling of targeted political discourse records to create a critical 40:1 class imbalance (200 Majority vs 5 Minority samples).
3. **Generative Feature Expansion:** A local generative pipeline executes iterative text transformations via customized, tone-locked prompting windows to preserve structural hooks (e.g., clickbait tendencies, sensationalist tone).
4. **Contextual Tokenization & Mapping:** Conversion of the balanced dataset arrays into native Hugging Face Arrow schemas with dynamic sentence padding/truncation to a maximum length of 256 tokens.
5. **Transformer Fine-Tuning:** Optimization of a `DistilBERT` sequence classifier across automated training epochs via the industrial Hugging Face `Trainer` API.
6. **Performance Diagnostics:** Structural evaluation yielding raw accuracy scores, classification metrics, and visual confusion arrays.

---

## ⚙️ Core Technical Stack

- **Data Engineering Core:** `Pandas`, `NumPy`, `Scikit-Learn`
- **Generative Backbone:** Hugging Face `transformers` API (`google/flan-t5-base`)
- **Classifier Backbone:** `distilbert-base-uncased`
- **Deep Learning Infrastructure:** `PyTorch` (Compatible with NVIDIA CUDA, Apple Silicon MPS, and CPU backends)
- **Data Visualizations:** `Matplotlib`, `Seaborn`, `Tabulate`

---

## 📊 Pipeline Diagnostic Report & Results

### 1. Dataset Balancing Transformation
The pipeline successfully intervened in a severely broken data matrix, restoring class equilibrium without requiring external manual annotation overhead:

- **Verified Science News (Majority Class):** 200 raw samples
- **Political Rumors (Initial Minority Class):** 5 raw samples *(Severe Data Scarcity)*
- **Injected LLM Synthetic Transformations:** 195 generated samples
- **Final Balanced Dataset Footprint:** 400 total samples *(Perfect 1:1 Class Ratio)*

### 2. Fine-Tuned DistilBERT Evaluation
By exposing the classifier to realistic synthetic variations during the training loop, the downstream model developed robust semantic boundaries, avoiding majority-class convergence.

#### **Classification Matrix Metrics (Test Split: 80 Samples)**

```text
                        precision    recall  f1-score   support

Verified Space Science       0.95      1.00      0.97        38
      Political Rumors       1.00      0.95      0.98        42

              accuracy                           0.97        80
             macro avg       0.97      0.98      0.97        80
          weighted avg       0.98      0.97      0.98        80
