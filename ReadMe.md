# 🩺 Breast Cancer Prediction (Analytics in Healthcare)

## 📌 Overview
This project applies **machine learning** to predict whether a breast tumor is **benign or malignant** using features extracted from digitized fine-needle aspiration (FNA) images.  
The workflow includes **data preprocessing, feature selection, model training, and evaluation** with multiple ensemble classifiers.

> ⚠️ **Disclaimer:** This project is for educational purposes only. It is not a medical device and must not be used for diagnosis or treatment.

---

## 🎯 Problem Statement
Develop a classification model that uses tumor measurement features to predict the diagnosis class (**benign** or **malignant**).

---

## 🔄 Workflow
1. Load and inspect dataset  
2. Clean and preprocess data  
3. Perform exploratory data analysis (EDA)  
4. Select top 5 features using `SelectKBest` (chi-squared test):  
   - `texture_mean`  
   - `area_mean`  
   - `concavity_mean`  
   - `area_se`  
   - `concavity_worst`  
5. Split dataset (70:30 train-test split)  
6. Train ensemble models  
7. Evaluate performance with accuracy, precision, recall, F1-score, ROC/AUC  

---

## 🤖 Models Explored
- Random Forest Classifier  
- Bagging Classifier (Decision Tree base)  
- AdaBoost Classifier  
- XGBoost Classifier  

**Result:** AdaBoost achieved the best performance among the evaluated models.

---

## 📊 Key Insights
- Feature selection improved interpretability  
- Ensemble methods provided robust performance  
- AdaBoost showed superior accuracy and balanced metrics  


