# 🔮 Customer Churn Classification

This notebook develops models to predict customer churn, using SMOTE (Synthetic Minority Oversampling Technique) to handle class imbalance and improve detection of churners.

---

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

## 📊 Results Summary

After balancing and tuning:

✅ Logistic Regression  
- Recall: **80%** on churners  
- Reasonable precision  

✅ SVM (C=0.5, RBF kernel)  
- Recall: **74%** on churners  

✅ KNN (9 neighbors, uniform weighting)  
- Recall: **76%** on churners  

These results prioritize catching churners (high recall) over purely maximizing accuracy, which better serves the business goal of customer retention.

---

## 📝 How to Run

1. Clone this repository  
2. Open the `.ipynb` notebook  
3. Run the cells in sequence  
4. Modify hyperparameters or test other balancing techniques if you want to explore further

---

*Notebook submitted as coursework.*
