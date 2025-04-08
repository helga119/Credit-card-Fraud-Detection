# Credit-card-Fraud-Detection

-Overview
This project focuses on detecting fraudulent credit card transactions using various machine learning algorithms. It compares the performance of three key models Random Forest, XGBoost, and Artificial Neural Networks -across different data balancing strategies: imbalanced, undersampled, and oversampled datasets.

-Models Used
Random Forest
XGBoost
Artificial Neural Network (ANN)

-Dataset
Source: Kaggle Credit Card Fraud Detection Dataset
Total records: 284,807
Fraudulent transactions: 473
All features are anonymized (V1–V28) using PCA
Class imbalance ratio is approximately 1:700

-Techniques Applied
Data Cleaning: Removal of duplicates
Feature Engineering: Added Hour and Is_Night from the Time column
Standardization: Applied StandardScaler to Amount and Is_Night
Balancing Methods:
Undersampling using RandomUnderSampler
Oversampling using SMOTE

-Evaluation Metrics
To properly evaluate performance on an imbalanced dataset:
Accuracy
Precision
Recall
F1-Score
Confusion Matrix

-Key Learnings
Imbalanced data significantly affects precision and recall.
Oversampling with SMOTE preserved data volume and improved ANN and Random Forest performance.
XGBoost handled imbalance naturally well, even without resampling.
