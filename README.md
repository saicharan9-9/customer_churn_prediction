# Customer Churn Prediction

## 📌 Project Overview

This project focuses on predicting customer churn using historical customer data.

The objective is to identify customers who are likely to leave a service or subscription and understand the factors associated with customer churn.

## 🎯 Objective

Build a machine learning classification model capable of identifying customers who are likely to churn.

## 📊 Dataset

The dataset contains customer-level information including demographic details, usage behavior, support interactions, payment behavior, subscription information, and spending.

### Features

- Age
- Gender
- Tenure
- Usage Frequency
- Support Calls
- Payment Delay
- Subscription Type
- Contract Length
- Total Spend
- Last Interaction

`CustomerID` was removed because it is only an identifier and does not provide meaningful predictive information.

## 🔍 Exploratory Data Analysis

The dataset was analyzed to understand:

- Data types
- Missing values
- Duplicate records
- Distribution of numerical features
- Categorical feature distributions
- Churn distribution
- Relationships between customer behavior and churn

## ⚙️ Data Preprocessing

The following preprocessing techniques were applied:

- Removal of unnecessary identifier columns
- Encoding of categorical variables
- Feature scaling where required
- Train-test split
- Handling class imbalance using SMOTE

### SMOTE

SMOTE was applied **only to the training data** after preprocessing to address class imbalance.

The test dataset was kept untouched for reliable model evaluation.

## 🤖 Machine Learning

The project applies supervised machine learning classification techniques to predict customer churn.

Models evaluated include:

- Logistic Regression

## 📈 Evaluation Metrics

The models are evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

For churn prediction, particular attention is given to **Recall**, since missing customers who are actually going to churn can be costly for a business.

## 📊 Results

The model was evaluated using Accuracy, Precision, Recall, and F1-Score.

| Metric | Score |
|--------|------:|
| **Accuracy** | **83.07%** |
| **Precision** | **80.62%** |
| **Recall** | **84.46%** |
| **F1-Score** | **82.50%** |

### Confusion Matrix

|  | Predicted: No Churn | Predicted: Churn |
|---|---:|---:|
| **Actual: No Churn** | 5558 | 1235 |
| **Actual: Churn** | 945 | 5137 |

### Metric Interpretation

- **Accuracy (83.07%)** — Overall percentage of correctly classified customers.
- **Precision (80.62%)** — Of the customers predicted to churn, 80.62% actually churned.
- **Recall (84.46%)** — Of the customers who actually churned, the model correctly identified 84.46%.
- **F1-Score (82.50%)** — Harmonic mean of Precision and Recall.

The model achieved a relatively balanced Precision and Recall, with Recall being particularly important for identifying customers at risk of churn.

## 💡 Key Findings

The project will analyze which customer characteristics and behaviors are most strongly associated with churn.

These findings can help businesses identify at-risk customers and develop targeted retention strategies.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- Jupyter Notebook

## 📁 Project Structure

```text
customer_churn_prediction/
│
├── Customer_Churn_Prediction.ipynb
├── customer_churn_dataset.csv
└── README.md
