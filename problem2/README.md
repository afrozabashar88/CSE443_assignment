# Project Overview
This project focuses on predicting whether a customer will subscribe to a term deposit (yes/no) based on bank marketing campaign data. The dataset contains demographic, financial, and campaign-related features.
The goal is to build a classification model and evaluate its performance while handling class imbalance effectively.

# Dataset Description
Dataset Name: Bank Marketing Dataset
Total Records: 45,211
Features: 17 columns
Target Variable: y (Yes = 1, No = 0)
# Key Features:
age: Customer age
job: Type of job
marital: Marital status
education: Education level
balance: Account balance
housing: Housing loan status
loan: Personal loan status
contact: Contact communication type
duration: Last contact duration
campaign: Number of contacts during campaign
poutcome: Outcome of previous campaign

# Methodology
## Data Preprocessing
Converted target variable (yes → 1, no → 0)
Applied One-Hot Encoding to categorical variables
Split dataset into train (80%) and test (20%)
Standardized features using StandardScaler

## Handling Class Imbalance
Dataset is highly imbalanced:
No: 39,922
Yes: 5,289
Used:
class_weight = 'balanced'
in Logistic Regression to improve minority class detection.

## Model Used
Logistic Regression
max_iter = 1000
class_weight = 'balanced'

# Model Evaluation
## Confusion Matrix
[[6715 1237]
 [ 185  906]]

#Performance Metrics
Metric
Class 0 (No)
Class 1 (Yes)
Precision
0.97
0.42
Recall
0.84
0.83
F1-score
0.90
0.56

# Overall Accuracy
Accuracy: 84.27%


# Key Insights
The model performs very well on majority class (No).
High recall (0.83) for 'Yes' class means:
→ Model successfully identifies most potential subscribers.
However, low precision (0.42) indicates:
→ Many false positives (predicting "Yes" when actually "No").

# Limitations
Logistic Regression struggles with:
Complex relationships
Imbalanced datasets (even with balancing)
Feature duration may introduce data leakage (post-contact info)


# Conclusion
This project demonstrates how Logistic Regression can be used for binary classification with imbalanced data. While accuracy is decent, improving precision for the minority class remains a key challenge.

👤 Author
Afroza


