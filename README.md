# Fraud_Detection
Real-time Financial Fraud Detection system for mobile money transactions. Implements Logistic Regression with balanced class weights to handle extreme data imbalance, feature engineering for balance discrepancies, and a Streamlit dashboard for instant fraud flagging.

🛡️ Financial Fraud Detection System

This project is an End-to-End Machine Learning application designed to identify fraudulent financial transactions. It features a data analysis pipeline, a trained classification model, and an interactive Streamlit web interface for real-time predictions.

📌 Project Overview

The goal of this project is to detect fraudulent patterns in mobile money transactions. Since fraud cases are typically rare (imbalanced data), the model uses specialized techniques to ensure high detection rates for suspicious activities.

Key Highlights:

Comprehensive EDA: Visualized transaction types, fraud distribution, and correlation matrices.

Feature Engineering: Calculated balance differences (balanceDiffOrig, balanceDiffDest) to identify anomalies.

Automated Pipeline: Integrated StandardScaler and OneHotEncoder into a Scikit-learn Pipeline for seamless data processing.

Deployment-Ready: A user-friendly web app built with Streamlit for manual transaction checking.

🛠️ Technical Stack

Language: Python 3.x

Data Analysis: Pandas, NumPy

Visualization: Matplotlib, Seaborn

Machine Learning: Scikit-learn (Logistic Regression, Pipelines)

Model Deployment: Streamlit, Joblib

📊 Model Performance

The model focuses on transaction types like TRANSFER and CASH_OUT, where fraud is most prevalent.

Algorithm: Logistic Regression with class_weight='balanced'.

Metric: Evaluated using Precision, Recall, and F1-Score via a Classification Report.

Logic: The model analyzes the relationship between the transaction amount and the change in account balances for both sender and receiver.

🚀 Getting Started

1. Prerequisites
Ensure you have Python installed. You can install the required dependencies using pip:

Bash
pip install pandas numpy matplotlib seaborn scikit-learn streamlit joblib

2. File Structure
AIML Dataset.csv: The raw transaction dataset.

train_model.py: Script for data cleaning, EDA, and model training.

fraud_detection_pipeline.pkl: The serialized model (generated after training).

fraud_detection.py: The Streamlit application script.

3. Running the Application
To launch the interactive web dashboard, run the following command in your terminal:

Bash
streamlit run "fraud detection.py"

🖥️ How to Use the App
Input Details: Enter the transaction type (e.g., TRANSFER, CASH_OUT).

Enter Amounts: Input the transaction amount and the account balances before/after the transaction.

Predict: Click the "Predict" button.

Result: * 🔴 Prediction: 1 — The system flags the transaction as Potential Fraud.

🟢 Prediction: 0 — The system marks the transaction as Legitimate.

📈 Future Enhancements

Advanced Models: Implementing Random Forest or XGBoost for higher accuracy.

SMOTE: Using Synthetic Minority Over-sampling Technique to better handle the data imbalance.

Real-time API: Converting the model into a REST API for integration with banking software.
