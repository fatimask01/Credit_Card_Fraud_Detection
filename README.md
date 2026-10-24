# Credit Card Fraud Detection

## Problem
Predict whether a credit card transaction is fraudulent or legitimate —
catching fraud before it costs the customer money.

## Data
- Source: [Kaggle — Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- Download creditcard.csv from the link above and place it in the project root before running the notebook.

## Method
- Normalised Amount and Time using StandardScaler
- Stratified 80/20 train-test split to preserve the fraud ratio
- Logistic Regression with class_weight='balanced' to handle severe class imbalance
- Priority metric: Recall — missing real fraud is costlier than a false alarm

## Results
| Metric           | Score  |
|------------------|--------|
| Accuracy         | 97.55% |
| Fraud Recall     | 0.92   |
| Fraud Precision  | 0.06   |
| Fraud F1-Score   | 0.11   |

The model correctly identified 90 out of 98 fraud cases in the unseen test set.

## Stack
Python, pandas, numpy, scikit-learn, matplotlib, seaborn

## Run It
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
jupyter notebook Credit_Card_Fraud_Detection_Structured_test.ipynb
```
> Place the dataset CSV in the same folder as the notebook before running.
