# Analytics in Healthcare: Breast Cancer Prediction

## 📌 Project Overview
This project applies **machine learning** to predict whether a breast tumor is **benign or malignant** using measurements extracted from digitized fine-needle aspiration (FNA) images of breast masses. The dataset features describe characteristics of cell nuclei, enabling predictive modeling for educational and research purposes.

> **Disclaimer:** This project is for educational purposes only. It is not a medical device and must not be used for diagnosis or treatment decisions.

---

## 🎯 Problem Statement
Develop a classification model that uses tumor measurement features to predict the diagnosis class (**benign** or **malignant**).

---

## 🔄 Machine Learning Workflow
1. Load and inspect the dataset.
2. Clean and prepare the data.
3. Perform exploratory data analysis (EDA) to examine feature relationships.
4. Select five key features using `SelectKBest` with the chi-squared test:
   - `texture_mean`
   - `area_mean`
   - `concavity_mean`
   - `area_se`
   - `concavity_worst`
5. Split the dataset into training and testing sets (70:30 split).
6. Train and compare ensemble classification models.
7. Evaluate performance using:
   - Confusion Matrix  
   - Classification Report  
   - ROC Curve / AUC  
   - Precision, Recall, Accuracy, F1-score  

---

## 🤖 Models Explored
- Random Forest Classifier  
- Bagging Classifier (Decision Tree base)  
- AdaBoost Classifier  
- XGBoost Classifier  

**Result:** AdaBoost achieved the best performance among the evaluated models based on the chosen metrics.

---

## 📂 Repository Structure
```text
analytics-healthcare/
├── Analytics in Healthcare.ipynb   # Jupyter notebook with full workflow
├── requirements.txt                # Python dependencies
└── README.md                       # Project documentation

