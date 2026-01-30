💳 Credit Card Fraud Detection using Machine Learning

This project demonstrates how to detect fraudulent credit card transactions using Machine Learning techniques.
The dataset is highly imbalanced, so the focus is on Precision, Recall, and F1-Score rather than accuracy.

📌 Dataset

Source: Kaggle – Credit Card Fraud Dataset

Target Column: Class

0 → Non-Fraud

1 → Fraud

The dataset contains anonymized numerical features generated using PCA.
Project Objectives

Understand class imbalance in fraud detection

Build a baseline classification model

Train an advanced ensemble model

Evaluate models using appropriate metrics

Identify important fraud indicators

Save the trained model for reuse
Technologies Used

Python

Pandas

NumPy

Scikit-Learn

Matplotlib

Joblib
🧪 Workflow
1️⃣ Load Dataset & Analyze Imbalance

Load CSV file using Pandas

Count fraud vs non-fraud transactions

Observe heavy class imbalance
2️⃣ Feature & Target Separation

Separate input features (X)

Separate target variable (y = Class)

Remove unnecessary identifier columns if needed
3️⃣ Stratified Train-Test Split

Split data into training and testing sets

Use stratified sampling to preserve fraud ratio
4️⃣ Baseline Model – Logistic Regression

Train Logistic Regression as a baseline

Use class_weight="balanced" to handle imbalance

Evaluate using Precision, Recall, and F1-Score
5️⃣ Advanced Model – Random Forest

Train Random Forest with:

n_estimators = 100

class_weight = "balanced"

Capture non-linear fraud patterns
6️⃣ Model Evaluation

Evaluate both models using:

Precision

Recall

F1-Score

Accuracy is avoided due to class imbalance
7️⃣ Feature Importance Analysis

Extract feature importance from Random Forest

Plot top fraud indicators using bar chart
8️⃣ Model Comparison
| Model               | Strength                               |
| ------------------- | -------------------------------------- |
| Logistic Regression | Simple baseline                        |
| Random Forest       | Better fraud detection & higher recall |

9️⃣ Save Best Model

Save trained Random Forest model using joblib

Enables reuse for future predictions or deployment
📊 Evaluation Metrics

Precision: Correctly predicted frauds

Recall: Fraud cases successfully detected

F1-Score: Balance between precision & recall

These metrics are crucial for real-world fraud detection.
Project Structure:

📦 Credit-Card-Fraud-Detection
 ┣ 📜 creditcard.csv
 ┣ 📜 fraud_detection.py
 ┣ 📜 credit_card_fraud_model.pkl
 ┣ 📜 README.md
▶️ How to Run
pip install pandas scikit-learn matplotlib joblib

python fraud_detection.py
🚀 Future Improvements

Apply SMOTE or undersampling techniques

Use XGBoost or LightGBM

Plot ROC-AUC curve

Deploy model using Flask or Streamlit

Real-time transaction prediction
Key Takeaways

Fraud detection is an imbalanced classification problem

Accuracy alone is misleading

Random Forest outperforms baseline model

Feature importance improves interpretability

Model persistence enables production use
