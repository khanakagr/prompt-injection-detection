# Prompt Injection Detection Using Machine Learning

## 📌 Overview

Large Language Models (LLMs) can be vulnerable to **prompt injection attacks**, where specially crafted inputs attempt to manipulate the model's intended behaviour or bypass its instructions.

This project develops a **machine learning-based approach for detecting prompt injection attacks** by analyzing prompts using multiple types of features — **lexical, linguistic, and semantic**.

The project was carried out as a **research internship project at Anveshan Foundation**, in a team of two, and was further developed into a research paper.

---

## 🎯 Objective

The main objective is to automatically classify a given prompt as either:

* **Benign** — a legitimate user prompt
* **Malicious** — a prompt containing potential injection behaviour

Rather than relying only on keywords, the project combines different characteristics of the input to capture both surface-level and deeper patterns associated with prompt injection attacks.

---

## 🔍 Methodology

The project follows a machine learning pipeline consisting of the following stages:

### 1. Data Preprocessing

The prompt dataset is cleaned and prepared for analysis before feature extraction and model training.

### 2. Feature Extraction

Three major categories of features are considered:

#### 🔤 Lexical Features

These capture characteristics of the words and tokens present in a prompt.

Examples include:

* TF-IDF features
* Word-level patterns
* Character-level patterns
* Frequency-based characteristics

#### 📝 Linguistic Features

These capture structural and linguistic properties of prompts.

Examples include:

* Prompt length
* Word and sentence statistics
* Punctuation patterns
* Other linguistic characteristics

#### 🧠 Semantic Features

These capture the contextual meaning of prompts using semantic representations.

Combining semantic information with lexical and linguistic characteristics helps the model identify attacks that may not be detectable through simple keyword matching.

---

## 🤖 Machine Learning Models

Multiple machine learning classifiers were trained and compared to determine which approach performs best for prompt injection detection.

The models were evaluated using standard classification metrics, including:

* Accuracy
* Precision
* Recall
* F1-score

The best-performing model achieved an **accuracy of 91.7%** on the evaluation data.

---

## 📊 Results

The comparative experiments showed that combining different feature types can effectively distinguish between benign and malicious prompts.

**Best Model Accuracy: 91.7%**

The project also focuses on **model interpretability**, allowing the characteristics contributing to the classification to be analyzed rather than treating the model purely as a black box.

---

## 🏗️ Project Pipeline

```text
                    Input Prompt
                         │
                         ▼
                Data Preprocessing
                         │
                         ▼
              Feature Extraction
                         │
          ┌──────────────┼──────────────┐
          ▼              ▼              ▼
      Lexical        Linguistic      Semantic
      Features       Features        Features
          │              │              │
          └──────────────┼──────────────┘
                         ▼
                  Feature Combination
                         │
                         ▼
               ML Model Training
                         │
                         ▼
                 Model Comparison
                         │
                         ▼
              Benign / Malicious
```

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **Natural Language Processing**
* **Machine Learning**
* **Text Feature Extraction**
* **Semantic Representations**

---

## 📄 Research Paper

The complete research paper is available in this repository:

**Prompt Injection Detection Using Lexical, Linguistic, and Semantic Features: A Comparative and Interpretable Machine Learning Study**

[📄 View Research Paper](./Prompt%20Injection%20Detection%20Using%20Lexical,%20Linguistic,%20and%20Semantic%20Features_%20A%20Comparative%20and%20Interpretable%20Machine%20Learning%20Study.pdf)

---

## 🚀 Future Improvements

* Evaluate the approach on larger and more diverse prompt injection datasets
* Test against newer and more sophisticated attack techniques
* Explore transformer-based classification models
* Improve detection of previously unseen attack patterns
* Develop the model as a real-time security layer for LLM applications

---

## 👩‍💻 Authors

**Khanak Agrawal**
