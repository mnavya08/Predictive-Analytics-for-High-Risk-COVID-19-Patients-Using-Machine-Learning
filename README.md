# 🧠 Predictive Modeling of High-Risk COVID-19 Patients Using Machine Learning

## 📌 Overview

This project leverages **Cerner's Real-World Data (CRWD)** to build predictive machine learning models that identify high-risk COVID-19 patients at the time of hospital admission. The model aims to support healthcare providers in making informed, early decisions to allocate resources efficiently and improve patient outcomes during pandemic situations.

> 🔍 **Key Goal**: Predict whether a patient is at high risk of mortality or ICU admission using only the data available **at the time of hospital encounter**.

---

## 🚀 Project Highlights

- 📊 **Data Size**: 11,580 records × 88 features  
- 🏥 **Domain**: Healthcare, Infectious Disease, COVID-19  
- ⚙️ **Tech Stack**: Python, Scikit-learn, CatBoost, XGBoost, LightGBM, SHAP, SMOTE  
- 🧠 **ML Techniques**: Feature selection with BORUTASHAP, Class balancing, Stratified cross-validation  
- 📈 **Best Model**: CatBoost (F1 Score: **0.86**, ROC AUC: **0.86**)

---

## 🧾 Problem Statement

> **How can we accurately identify COVID-19 patients at higher risk of severe outcomes (death or ICU) using only pre-admission features from hospital data?**

Predicting early helps clinicians make timely interventions and manage hospital capacity during pandemics.

---

## 🧰 Tools & Technologies

| Area            | Tools Used                                                                  |
|-----------------|-----------------------------------------------------------------------------|
| Data Handling   | Pandas, NumPy, Scikit-learn                                                 |
| Imputation      | KNN Imputer, Little’s MCAR Test                                             |
| Visualization   | Matplotlib, Seaborn, SHAP                                                   |
| ML Algorithms   | Logistic Regression, Random Forest, CatBoost, XGBoost, LightGBM             |
| Balancing       | SMOTE, RandomUnderSampler (from imbalanced-learn)                           |
| Feature Selection| SHAP, BORUTASHAP                                                           |

---

## 📊 Data Preprocessing

- Removed post-admission, identifier, and sparse (>70% missing) columns.
- Handled missing values using **KNN Imputer** after verifying with **Little's MCAR test**.
- Encoded categorical variables and mapped ICD disease codes for interpretability.
- Balanced the binary target variable (`deceased`) using **SMOTE + undersampling**.

---

## 📉 Model Building & Evaluation

Implemented 5 models using **Stratified 5-Fold Cross Validation** and evaluated using:

- **Accuracy**
- **Precision**
- **Recall**
- **F1 Score**
- **ROC AUC**

### 🏆 Best Model: CatBoost

| Metric     | Score  |
|------------|--------|
| Accuracy   | 0.86   |
| F1 Score   | 0.86   |
| Precision  | 0.84   |
| Recall     | 0.88   |
| ROC AUC    | 0.86   |

---

## 🔍 Model Interpretability with SHAP

Used SHAP to explain model decisions:

- Global feature importance plots
- SHAP Summary Plot
- Feature value impacts

**Top Predictors**:
- Genitourinary diseases
- Encounter route & type
- Parasitic/Respiratory conditions
- Age at encounter

---



