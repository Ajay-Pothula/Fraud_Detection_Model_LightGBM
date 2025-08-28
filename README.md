# Fraud_Detection_Model_LightGBM

This repository contains a **machine learning-based fraud detection system** using **LightGBM**. The model is designed to identify fraudulent transactions with high accuracy, recall, and precision, while maintaining robustness to class imbalance.


## 📌 Project Overview

Fraud detection is a critical task in banking, insurance, and e-commerce industries. Fraudulent activities cause massive financial losses every year. This project builds a **binary classification model** to distinguish between **fraudulent (1)** and **non-fraudulent (0)** transactions.

We use:
- **LightGBM** for fast, scalable gradient boosting.
- **Stratified train-test splits** to handle class imbalance.
- **Custom threshold tuning** for maximizing F1-score.
- **Feature importance analysis** to understand key drivers of fraud.

---

## 📊 Dataset

The Dataset is very large and it is not being uploaded in the github so im uploading just some rows here.
- Each row represents a transaction.
- Features include transaction details (amount, frequency, account activity, etc.).
- Target variable:
  - `0` → Legitimate transaction  
  - `1` → Fraudulent transaction


⚠️ Note: Dataset is not included here for confidentiality reasons. Replace with your dataset before running.

---

## ⚙️ Model Workflow

1. **Data Preprocessing**
   - Handle missing values
   - Standardize/normalize numerical features
   - Encode categorical features (if any)

2. **Train-Test Split**
   - Stratified split ensures balance in fraud vs. non-fraud across train/validation.

3. **Model Training**
   - LightGBM with:
     - `auc` as evaluation metric
     - Early stopping (50 rounds)
   - Hyperparameters tuned for performance

4. **Model Evaluation**
   - AUC (Area Under Curve)
   - Binary Log Loss
   - Confusion Matrix
   - Precision, Recall, F1-score
   - Feature Importance Ranking

5. **Threshold Tuning**
   - Default threshold of `0.5` adjusted for best F1 score
   - Best threshold found at `0.88`

---

## 📈 Results

- **Best F1 Score**: `0.8669` at threshold `0.88`  
- **AUC**: `0.9995`  
- **Classification Report:**
  - Precision (Fraud): **0.93**
  - Recall (Fraud): **0.82**
  - Accuracy: **99.97%**
- **Confusion Matrix:**
