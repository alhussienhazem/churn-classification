# 🔮 Customer Churn Classification

**Workshop Homework Submission**

This notebook develops machine learning models to predict customer churn, using SMOTE (Synthetic Minority Oversampling Technique) to address class imbalance and improve churner detection.

---

## 📚 Table of Contents

- [🚀 Installation](#-installation)
- [🎯 Project Goals](#-project-goals)
- [⚙️ Methods](#-methods)
- [📊 Results](#-results)
- [📝 Submission Notes](#-submission-notes)

---

## 🚀 Installation

- **Requirements:** Python 3.8+, Jupyter Notebook

```bash
# Clone the repository
git clone https://github.com/alhussienhazem/churn-classification.git

# Navigate to the project folder
cd churn-classification

# (optional) create a virtual environment
python -m venv venv
source venv/bin/activate  # on Linux/Mac
venv\Scripts\activate     # on Windows

# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook
```
---

## 🎯 Project Goals

- **Objective:** Predict customer churn with high recall, prioritizing identifying true churners.
- **Challenge:** Imbalanced data with far fewer churn samples than non-churn samples.
- **Solution:** Apply SMOTE to oversample the minority class in training data, boosting the ability to detect churners.

---

## ⚙️ Methods

- **Models Used:**
  - Logistic Regression
  - Support Vector Machine (SVM)
  - K-Nearest Neighbors (KNN)

- **Techniques Applied:**
  - SMOTE to balance classes
  - MinMax scaling for feature normalization
  - Evaluation with precision, recall, F1-score (not just accuracy)
  - Confusion matrices for visualization

---

## 📊 Results

| Model                | Accuracy | Churn Precision | Churn Recall | Churn F1-score |
|----------------------|----------|-----------------|--------------|----------------|
| Logistic Regression  | 75.2%    | 0.47            | 0.78         | 0.59           |
| SVM                  | 76.5%    | 0.49            | 0.74         | 0.59           |
| KNN                  | 69%      | 0.41            | 0.76         | 0.53           |

- **Key Insight:**
  - All models achieved over 74% recall on churners, which is essential for a retention-driven business.
  - Among them, SVM showed the best balanced accuracy.

---

## 📝 Submission Notes

- Notebook cells are cleaned, ordered, and reproducible
- `requirements.txt` included for environment setup
- Dataset assumed to be placed in a `data/` folder (if public)
- Notebook submitted as part of workshop coursework
  
---
> *Notebook submitted as coursework.*

