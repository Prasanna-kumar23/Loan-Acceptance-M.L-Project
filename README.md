# Loan Acceptance Prediction (Python + Machine Learning)
Machine Learning Project to Predict whether a bank customer will accept a personal loan offer

## Problem
Predict whether a customer will accept a personal loan.

Target: Personal Loan –
1 = Loan Accepted, 0 = Loan Not Accepted

##This helps the bank to:
- Target the right customers for marketing campaigns
- Reduce cost of offers that are unlikely to be accepted
- Improve overall conversion rate for loans

## Models used
- I implemented and compared two classification models:
- Logistic Regression - Baseline interpretable model
- Evaluated with accuracy, recall, confusion matrix, ROC curve

Decision Tree Classifier
- Non-linear model that can capture complex relationships
- Also evaluated with accuracy, recall, confusion matrix, ROC curve
- Both models use the same train/test split and preprocessing to make a fair comparison.

## Tools
- Python
- Scikit-learn
- Pandas
- Google Colab

## Steps
- Data preprocessing
- Feature engineering
- Model training (Logistic Regression + Decision Tree)
- Evaluation & Comparision

## Results

**Test set performance (test_size = 0.2):**

| Model              | Accuracy (Test) | Recall – Loan Accepted (Test) | AUC-ROC (Test) |
|--------------------|-----------------|-------------------------------|----------------|
| Logistic Regression| 0.90            | 0.90                          | 0.96           |
| Decision Tree      | 0.95            | 0.94                          | 0.98           |

