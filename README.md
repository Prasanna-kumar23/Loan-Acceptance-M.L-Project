# Personal Loan Acceptance Prediction (Python + Machine Learning)

In this project, I built a machine learning model to predict whether a bank customer will **accept a personal loan offer**.  
The goal is to help the bank target the right customers, reduce marketing costs and improve campaign efficiency.

## Problem I Worked On

A retail bank has a large base of existing customers. The bank wants to know:

**Which existing customers are most likely to accept a personal loan offer**

Instead of sending the offer to everyone, the bank wants to focus on customers with a high probability of accepting the loan.

This becomes a **binary classification problem**:  
- '1' = customer accepts the loan  
- '0' = customer does not accept the loan  

## What I Did

### Exploratory Data Analysis (EDA)

- Checked data types, missing values, and basic statistics.
- Looked at the **distribution of the target (Personal Loan)** to understand class balance.
- Explored relationships between the target and key features like:
  - Income
  - Average spending on credit cards
  - Education level
  - Existing products (CD account, online, credit card)
- Created plots to see which customer profiles are more likely to accept a loan.

### Data Preprocessing

- Selected relevant features for modeling.
- Performed encoding / transformation where needed.
- Split the data into **training and test sets** with stratification so the class distribution is similar in both.
- Handled class imbalance using options like:
- class_weight='balanced' (for some models)
    
### Models I Trained

I compared multiple classification models:

1. **Logistic Regression**  
   - Used as a baseline model to capture the relationship between features and the probability of accepting a loan.

2. **Decision Tree Classifier**  
   - Captures non-linear relationships and simple decision rules.
   - Easy to interpret which splits/features are important.

I used helper functions in my notebook to:
- Train each model
- Evaluate performance on train and test sets
- Compare different **test sizes**
- Store the results in summary tables

### Model Evaluation

For each model, I looked at:

- **Accuracy**
- **Recall for the positive class (loan accepted)** – important so we don’t miss too many potential customers
- **Confusion matrix**
- **Classification report (precision, recall, F1-score)**
- **ROC curve and AUC**

Using these metrics, I compared Logistic Regression and Decision Tree to see which model gives the best balance between correctly identifying likely loan-acceptors and avoiding too many false positives.

## Results

**Test set performance (test_size = 0.2):**

| Model              | Accuracy (Test) | Recall – Loan Accepted (Test) | AUC-ROC (Test) |
|--------------------|-----------------|-------------------------------|----------------|
| Logistic Regression| 0.90            | 0.90                          | 0.96           |
| Decision Tree      | 0.95            | 0.94                          | 0.98           |

