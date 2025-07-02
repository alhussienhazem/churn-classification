# 🔮 Customer Churn Classification

This notebook develops models to predict customer churn, using SMOTE (Synthetic Minority Oversampling Technique) to handle class imbalance and improve detection of churners.

---

## 📚 Table of Contents

- [Installation](#-installation)
- [Models Used](#-models-used)
- [Why Balance the Data?]#️-why-balance-the-data)
- [Results Summary](#-results-summary)
- [How to Run](#-how-to-run)

---

## 🚀 Installation

To set up the project locally, follow these steps:

```bash
# Clone the repository
git clone https://github.com/alhussienhazem/churn-classification.git

# Navigate to the project folder
cd churn-classification

# (Recommended) create a virtual environment
python -m venv venv
source venv/bin/activate  # on Linux/Mac
venv\Scripts\activate     # on Windows

# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook
```

## 🚀 Models Used

- Logistic Regression
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)

---

## ⚖️ Why Balance the Data?

In churn data, most customers do **not** churn, making the dataset imbalanced.  
Without balancing, models tend to ignore the churn class.  

SMOTE was applied to create synthetic churn examples in the training data, improving the model’s recall on churners.

---

## 📊 Results Summary (with SMOTE)

| Model | Accuracy | Churn Precision | Churn Recall | Churn F1-score |
|-------|----------|-----------------|--------------|----------------|
| **Logistic Regression** | 75.2% | 0.47 | 0.78 | 0.59 |
| **SVM**                 | 76.5% | 0.49 | 0.74 | 0.59 |
| **KNN**                 | 69%   | 0.41 | 0.76 | 0.53 |

---

These results prioritize catching churners (high recall) over purely maximizing accuracy, which better serves the business goal of customer retention.

---

## 📝 How to Run

1. Clone this repository  
2. Open the `.ipynb` notebook  
3. Run the cells in sequence  
4. Modify hyperparameters or test other balancing techniques if you want to explore further

---

> *Notebook submitted as coursework.*
