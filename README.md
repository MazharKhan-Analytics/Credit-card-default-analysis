# Credit-card-default-analysis
Credit Card Default Prediction
A machine learning project to predict credit card default risk using the UCI Credit Card Default dataset.

📊 Project Overview
This project analyzes credit card default patterns and builds predictive models to identify customers at high risk of defaulting on their credit card payments. The dataset contains 30,000 customer records with 25 features including demographic information, payment history, bill statements, and payment amounts.

🎯 Business Problem
Credit card defaults pose significant financial risks to banks and financial institutions. Early identification of potential defaulters can help institutions:

Reduce financial losses

Implement proactive risk management

Optimize credit limit decisions

Develop targeted customer retention strategies

📁 Dataset
Source: UCI Credit Card Default Dataset
Records: 30,000
Features: 25 original features
Target Variable: default.payment.next.month (Binary: 1 = Default, 0 = No Default)

Key Features:
Demographic: LIMIT_BAL, SEX, EDUCATION, MARRIAGE, AGE

Payment History: PAY_0 to PAY_6 ( repayment status)

Bill Amounts: BILL_AMT1 to BILL_AMT6

Payment Amounts: PAY_AMT1 to PAY_AMT6

🛠️ Technical Implementation
Data Preprocessing
✅ Missing value analysis (No missing values found)

✅ Categorical variable encoding

✅ Outlier treatment using RobustScaler

✅ Feature engineering (37 total features created)

Feature Engineering
Credit Utilization Metrics: avg_bill_ratio, max_bill_ratio

Payment Behavior: avg_payment_ratio, missed_payment_count

Delinquency Metrics: max_delay, avg_delay, num_delays

Customer Segmentation: is_young_customer, is_senior_customer

Financial Summary: avg_bill_amt, avg_pay_amt, pay_to_limit_ratio

Exploratory Data Analysis
Target variable distribution: 22.12% default rate

Credit limit analysis and distribution

Demographic insights

Payment pattern analysis

📈 Model Performance
(To be updated after model implementation)

🚀 Installation
# Clone the repository
git clone https://github.com/yourusername/credit-card-default-prediction.git

# Navigate to project directory
cd credit-card-default-prediction

# Install required packages
pip install -r requirements.txt

📋 Requirements
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
scikit-learn>=1.0.0
jupyter>=1.0.0

💻 Usage
# Load and preprocess data
from src.data_preprocessing import load_and_clean_data
df = load_and_clean_data('path/to/UCI_Credit_Card.csv')

# Feature engineering
from src.feature_engineering import create_features
df_processed = create_features(df)

# Train model
from src.model import train_model
model, scores = train_model(df_processed)

📁 Project Structure
credit-card-default-prediction/
│
├── data/
│   └── UCI_Credit_Card.csv
│
├── notebooks/
│   └── UCI_Credit_Card_Default.ipynb
│
├── src/
│   ├── __init__.py
│   ├── data_preprocessing.py
│   ├── feature_engineering.py
│   ├── model.py
│   └── utils.py
│
├── models/
│   └── (saved models)
│
├── requirements.txt
├── README.md
└── .gitignore

🔮 Future Enhancements
Implement multiple machine learning models

Hyperparameter tuning and cross-validation

Model interpretation using SHAP values

Deployment as a web application

Real-time prediction API

🙏 Acknowledgments
UCI Machine Learning Repository for the dataset

Contributors and maintainers of the open-source libraries used
