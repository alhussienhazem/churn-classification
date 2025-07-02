# 🔮 Customer Churn Classification

This notebook builds machine learning models to predict customer churn, applying SMOTE (Synthetic Minority Oversampling Technique) to address class imbalance and improve the detection of churned customers.

---

## 📚 Table of Contents

- [🚀 Installation](#-installation)
- [🎯 Project Goals](#-project-goals)
- [⚙️ Methods](#%EF%B8%8F-methods)
- [📊 Results](#-results)
- [📝 Project Details](#-project-details)
- [📜 License](#-License)

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

## 📝 Project Details

- All notebook cells are clean, ordered, and fully reproducible  
- Dependencies are listed in `requirements.txt` for quick setup  
- If a dataset is included, it should be placed in the `data/` folder  
  
---
## 📜 License

This project is for educational and non-commercial use only.  
The dataset used is the publicly available IBM Telco Customer Churn dataset, available here:  
[https://www.ibm.com/communities/analytics/watson-analytics-blog/guide-to-sample-datasets/](https://www.ibm.com/communities/analytics/watson-analytics-blog/guide-to-sample-datasets/)
