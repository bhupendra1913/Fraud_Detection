# Fraud_Detection
Real-time Financial Fraud Detection system for mobile money transactions. Implements Logistic Regression with balanced class weights to handle extreme data imbalance, feature engineering for balance discrepancies, and a Streamlit dashboard for instant fraud flagging.

💳 Credit Risk Modeling & Prediction

A comprehensive End-to-End Machine Learning project to analyze and predict credit risk using the German Credit Dataset. The project includes a detailed Exploratory Data Analysis (EDA), model optimization using GridSearchCV, and a web-based prediction app built with Streamlit.

📌 Project Overview

The goal of this project is to classify whether a person represents a Good or Bad credit risk based on various attributes like age, job, housing, saving accounts, and credit amount. This is a classic binary classification problem in the financial domain.

📊 Key Features

Data Cleaning: Handled missing values and dropped redundant columns.

EDA: Visualized distributions, correlations, and relationships between features using Seaborn and Matplotlib.

Feature Engineering: Label Encoding for categorical variables.

Model Comparison: Evaluated multiple models including:

Decision Tree

Random Forest

Extra Trees (Best Performing)

XGBoost

Hyperparameter Tuning: Used GridSearchCV to find the best model parameters.

Web App: Created a user-friendly interface using Streamlit for real-time predictions.

🛠️ Tech Stack

Language: Python

Libraries: Pandas, NumPy, Matplotlib, Seaborn

Machine Learning: Scikit-learn, XGBoost

Deployment: Streamlit

Model Persistence: Joblib

🚀 Installation & Usage

1. Clone the repository

git clone https://github.com/your-username/credit-risk-modeling.git
cd credit-risk-modeling

2. Install Dependencies

pip install pandas numpy matplotlib seaborn scikit-learn xgboost streamlit joblib

3. Run the Streamlit App

streamlit run app.py

📉 Analysis Insights

Credit Amount vs Age: Older individuals tend to apply for lower credit amounts, while younger individuals show a wider variance.

Risk Distribution: The dataset shows the relationship between "Duration" of credit and the risk level, where longer durations often correlate with higher risk.

Top Model: The Extra Trees Classifier was selected as the final model due to its superior performance on the test set.

📂 Project Structure
Plaintext
├── german_credit_data.csv       # Dataset
├── analysis_model.ipynb         # EDA and Model Training script
├── app.py                       # Streamlit Web Application
├── extra_trees_credit_model.pkl # Saved ML Model
├── *_encoder.pkl                # Saved Label Encoders
└── README.md                    # Project Documentation

🖥️ How it Works

Enter the applicant's details (Age, Sex, Job, Housing, etc.) in the Streamlit sidebar/form.

The app loads the pre-trained ExtraTreesClassifier and the saved LabelEncoders.

Click the Predict Risk button.

The app displays whether the credit risk is GOOD (Success) or BAD (Error).

Future Enhancements

Implementing SMOTE to handle class imbalance more effectively.

Adding more financial features to improve model accuracy.

Deploying the app to Streamlit Cloud or Heroku.
