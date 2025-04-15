# Credit-card-Fraud-Detection

-Overview
This project focuses on detecting fraudulent credit card transactions using various machine learning algorithms. It compares the performance of three key models Random Forest, XGBoost, and Artificial Neural Networks -across different data balancing strategies: imbalanced, undersampled, and oversampled datasets.

Dataset Summary
Source: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
Records: 284,807 transactions
Fraudulent transactions: 492
Class Distribution:
Class 0: Legitimate
Class 1: Fraud
-Features:
V1 to V28: Anonymized features from PCA
Time: Seconds since first transaction
Amount: Transaction amount
Class: Target label (1 = fraud, 0 = non-fraud)

Preprocessing Steps:
1.Load & Inspect Data
Removed duplicate entries
Checked for missing values

2.Feature Engineering
Created Hour from Time
Created binary feature Is_Night (1 if transaction time is between 9PM-6AM)

3.Data Scaling:
Used StandardScaler on Amount and Is_Night for normalization
Fit on training data and applied to both train/test sets

4.Class Imbalance Handling:
Undersampling using RandomUnderSampler
Oversampling using SMOTE

Models Trained
1.Random Forest Classifier
-Bagging-based ensemble method
-Tested with multiple max_depth values and estimators

2.XGBoost Classifier
-Boosting-based model that improves on previous errors
-Tuned learning_rate and max_depth

3.Artificial Neural Network
-Feed-forward deep neural network using Keras
-Includes dropout layers for regularization

Evaluation Metrics
Accuracy: Overall correctness of the model
Precision: How many predicted fraud cases were correct
Recall: How many actual frauds were caught
F1-score: Balance between precision and recall
AUC: Measures ability to separate fraud vs. non-fraud

Model Comparisons
Each model is trained on:
Imbalanced Dataset
Undersampled Dataset
SMOTE Oversampled Dataset

Performance is compared using:
Confusion Matrices
ROC Curves
Metric Plots (Accuracy, Precision, Recall, F1)

Final results show Random Forest with SMOTE performs best with an AUC of 0.98, balancing high recall and precision.

Ethical Considerations
-Dataset is anonymized using PCA to protect identities
-No personally identifiable information is exposed
-Used strictly for educational and academic purposes


