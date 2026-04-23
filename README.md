# Credit-Card-Fraud-Analysis using Machine Learning

 "Python" (https://img.shields.io/badge/Python-3.10-blue?logo=python)<br>
 "ML" (https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)<br>
"Status" (https://img.shields.io/badge/Status-Completed-brightgreen)<br>

---

Overview

Credit card fraud detection is a high-impact real-world problem involving highly imbalanced data. This project builds machine learning models to detect fraudulent transactions while balancing recall and precision.

---

Dataset

- Source: Kaggle Credit Card Fraud Dataset
- Link: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
- Total Transactions: 284,807
- Fraud Cases: 0.17%

Features:

- PCA-transformed features (V1 – V28)
- Time, Amount
- Target:
  - 0 → Legitimate
  - 1 → Fraud

---

Models Implemented

Logistic Regression

- Baseline model
- High recall for fraud detection
- Lower precision due to false positives

Random Forest Classifier

- Ensemble learning method
- Strong balance between precision and recall
- More suitable for practical deployment

---

Evaluation Metrics

- Precision
- Recall
- F1-Score
- ROC-AUC
- Average Precision (AUPRC)
- Confusion Matrix

---

Results

Overall Performance

Model| AUPRC| ROC-AUC
Logistic Regression| 0.709| 0.9699
Random Forest| 0.869| 0.9573

---

Detailed Performance

Logistic Regression

- Precision (Fraud): 0.0579
- Recall (Fraud): 0.9184
- F1-Score: 0.1090

Confusion Matrix:

[[55400  1464]
 [    8    90]]

Interpretation:
High recall indicates most fraudulent transactions are detected, but low precision leads to many false positives.

---

Random Forest

- Precision (Fraud): 0.9615
- Recall (Fraud): 0.7653
- F1-Score: 0.8523

Confusion Matrix:

[[56861     3]
 [   23    75]]

Interpretation:
High precision and strong F1-score indicate a better balance, making this model more practical for deployment.

---

Key Insights

- Logistic Regression is recall-oriented and useful when missing fraud is costly
- Random Forest provides a better balance between precision and recall
- Model choice depends on business priorities (false positives vs missed fraud)

---


Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

---

How to Run

git clone https://github.com/Srushti-J/Credit-Card-Fraud-Analysis.git<br>
cd Credit-Card-Fraud-Analysis<br>
pip install -r requirements.txt<br>
jupyter notebook analysis.ipynb

---

Future Work

- Implement XGBoost / LightGBM
- Perform hyperparameter tuning
- Build a real-time fraud detection pipeline
- Deploy using Streamlit or Flask

---

Author

Srushti Joshi

---

Note

Dataset is not included due to size constraints. Please download it from Kaggle using the link above.
