# 🔮 Customer Churn Prediction - Workshop Submission

**Course:** [Workshop Name]  
**Author:** [Your Name]  
**Date:** [Submission Date]  

![Churn Prediction Visualization](https://via.placeholder.com/800x400?text=Churn+Prediction+Analysis)  
*Example visualization from the analysis*

---

## 📚 Table of Contents
1. [Project Overview](#-project-overview)
2. [Key Features](#-key-features)
3. [Installation Guide](#-installation-guide)
4. [Methodology](#-methodology)
5. [Results & Insights](#-results--insights)
6. [How to Reproduce](#-how-to-reproduce)
7. [Submission Details](#-submission-details)

---

## 🌟 Project Overview

This project develops machine learning models to predict customer churn, addressing the critical business challenge of customer retention. The solution focuses on:

- Handling severe class imbalance using **SMOTE** (Synthetic Minority Oversampling Technique)
- Comparing performance of three classification algorithms
- Optimizing for **recall** to maximize identification of potential churners

---

## ✨ Key Features

- **Data Processing:**
  - Automated feature scaling (MinMaxScaler)
  - Strategic train-test splitting (80-20 ratio)
  - SMOTE oversampling (only applied to training set)

- **Model Comparison:**
  - Logistic Regression (baseline)
  - Support Vector Machine (RBF kernel)
  - K-Nearest Neighbors (K=5)

- **Evaluation Focus:**
  - Recall-oriented metrics
  - Balanced accuracy scores
  - Comparative performance analysis

---

## 🛠 Installation Guide

### Prerequisites
- Python 3.8+
- pip package manager
- Jupyter Notebook

### Setup Instructions
```bash
# 1. Clone repository
git clone https://github.com/alhussienhazem/churn-classification.git
cd churn-classification

# 2. Create and activate virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate    # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch Jupyter Notebook
jupyter notebook
```

🔬 Methodology
Data Pipeline
Preprocessing:

Missing value handling

Categorical feature encoding

Feature scaling (MinMaxScaler)

Class Imbalance Solution:

python
from imblearn.over_sampling import SMOTE
smote = SMOTE(sampling_strategy='minority', random_state=42)
X_train_res, y_train_res = smote.fit_resample(X_train, y_train)
Model Training:

5-fold cross-validation

Hyperparameter tuning (basic grid search)

Balanced accuracy optimization

📈 Results & Insights
Performance Comparison
Model	Accuracy	Precision	Recall	F1-Score	AUC-ROC
Logistic Regression	75.2%	0.47	0.78	0.59	0.82
SVM (RBF Kernel)	76.5%	0.49	0.74	0.59	0.83
KNN (K=5)	69.0%	0.41	0.76	0.53	0.79
Key Findings
Best Overall Performer: SVM achieved highest balanced accuracy (76.5%)

Best Recall: Logistic Regression identified 78% of churners

Trade-off Analysis: Higher recall came at cost of more false positives

