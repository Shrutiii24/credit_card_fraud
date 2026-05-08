# 💳 Credit Card Fraud Detection System

A Machine Learning project focused on detecting fraudulent credit card transactions using imbalance-aware modeling techniques and fraud-focused evaluation metrics.
## Project Overview

This project analyzes a highly imbalanced financial transaction dataset to identify fraudulent credit card transactions. Multiple Machine Learning models were implemented and compared to build an effective fraud detection pipeline.

The project focuses on:
- Fraud detection
- Imbalanced data handling
- Model comparison
- Threshold tuning
- Precision-recall optimization

## Dataset Information

The dataset contains anonymized credit card transaction records with:
- PCA-transformed features (`V1` to `V28`)
- Transaction `Amount`
- Transaction `Time`
- Target variable:
  - `0` → Legitimate Transaction
  - `1` → Fraudulent Transaction

Since fraudulent transactions represent less than 1% of the dataset, handling class imbalance was one of the major challenges of the project.

## Project Workflow

### 1. Exploratory Data Analysis (EDA)
- Analyzed class imbalance
- Visualized fraud vs non-fraud distributions
- Performed correlation analysis
- Identified important fraud-related features

### 2. Data Preprocessing
- Train-test split using stratified sampling
- Feature scaling using `StandardScaler`
- SMOTE applied for class imbalance handling

### 3. Model Building
Implemented and compared:
- Logistic Regression
- Random Forest Classifier
- XGBoost Classifier

### 4. Model Evaluation
Models were evaluated using:
- Precision
- Recall
- F1-Score
- ROC-AUC Score
- Confusion Matrix
- Precision-Recall Curve

### 5. Threshold Tuning
Custom probability thresholds were used to optimize the precision-recall tradeoff and reduce false positives.

## Key Findings

- Logistic Regression achieved high recall but generated many false positives.
- Random Forest provided the best balance between fraud detection and false alarm reduction.
- Threshold tuning improved Random Forest precision from **79% to 87%**.
- XGBoost achieved strong recall but lower precision compared to Random Forest.
- Features such as `V14`, `V17`, `V12`, and `V10` showed strong fraud-related patterns.

### Final Selected Model
**Threshold-Tuned Random Forest Classifier**

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Imbalanced-learn (SMOTE)
- Google Colab
