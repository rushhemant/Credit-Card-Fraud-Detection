# Credit-Card-Fraud-Detection
The aim of this project is to predict fraudulent credit card transactions using machine learning models.    The data set that we will be working on during this project was obtained from Kaggle. It contains thousands of individual transactions that took place over a course of two days and their respective labels.

**Problem Statement:**
# Credit Card Fraud Background
Credit Card Fraud is notable issue in banking industry. Increase in digitalization has led to more people using internet for online purchase. Apart from help build credit history Credit card offer other benefits like rewards, bonuses, emi option, cash back which makes it not only convenient but also lucrative option. Unfortunately, digital payment options have a downside since they are exposed to fraudsters to commit Credit Card fraud. Credit Card fraud is when an unauthorized transaction is made which can be result of either loss of physical card or theft of information. Fraud has an impact on both financial institute as well as consumer.

# Impact on financial institute:
1. Monetary loss
2. Reputational loss
3. Legal lawsuit

# Impact on consumer:
1. Monetary loss
2. Loss of faith

# Fraud Data
1. Data spread across 2 days in September 2013
2. There are total 284807 transactions out if which 492 are fraud transactions. This amounts to only 0.17275%.
3. Data is highly imbalanced and training model on this data will result in incorrect predictions. Even if model predicts all 0s (i.e. non-fraud) the accuracy will be 99.82725%.
4. Data provided had PCs of actual data except for column time, class (target variable) and amount.

# Objective
1. Predict fraudulent transactions.
2. Use right metric for model evaluation.
a. Missing out on reporting fraudulent transaction might result in huge monetary losses, reputation loss and legal lawsuit.
b. Reporting extra fraud transactions (False Positives) will result in higher operation cost for financial institute.

# Approach:
# Data Cleaning and Preparation
1. Data is high imbalanced. Building model using such data will result in biased model. We will use one of the below techniques for treat data imbalance issue.
a. Random Oversampling
b. SMOTE – Create synthetic data using SMOTE technique which will add data for minority class.
c. ADASYS – Similar to SMOTE adds minority data however using density distribution.
2. Data is skewed and hence we will use sklearn preprocessing package powertransformer to make the distribution more gaussian. Skewed data may impact model output especially for models that are sensitive to outliers.
# Model Building and Training
1. This is a classification problem and we will try various classification models.
a. KNN
b. SVM
c. Decision Tree
d. Random Forest
e. XGBoost
2. We will build model with or without balancing technique to understand impact of data imbalance.
3. We will tune the hyper parameters using Randomized search CV and cross-validation to test out model.
# Evaluation
There are various metrics available for classification problem, but we will have to choose metric properly.
1. Accuracy – Correctly predicted labels
2. Sensitivity – Correctly predicted Yes
3. Specificity – Correctly predicted Nos
4. ROC Curve – TPR vs FPR
We will use ROC for our evaluation.
