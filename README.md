# 💳 Credit Card Default Prediction – End-to-End Machine Learning Project

## 📌 Project Overview
This project predicts whether a customer is likely to **default on their next month’s credit card payment** using machine learning techniques.  
The analysis uses the **UCI Credit Card Default Dataset**, which contains demographic data, credit limits, bill history, and payment behavior for 30,000 customers.

The goal is to help financial institutions reduce risk by identifying **high-risk customers early**, enabling better credit decisions, targeted interventions, and portfolio stability.

---

## 🎯 Objectives
- Build a predictive model for **credit card default risk**
- Analyze customer behavior patterns influencing defaults
- Engineer relevant features for improved model accuracy
- Compare models (Random Forest & XGBoost)
- Generate interpretable insights using feature importance
- Prepare data for BI dashboards (Power BI)
- Export final cleaned dataset with model-generated risk scores

---

## 📂 Project Workflow

### **1. Import Libraries**
Used major data science packages:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `sklearn`
- `xgboost`

---

### **2. Load Dataset**
Imported UCI dataset and verified structure, data types, and null values.

---

### **3. Rename Columns**
Applied readable and business-friendly column names:
- `SEX` → `Gender`
- `EDUCATION` → `Education_Level`
- `MARRIAGE` → `Marital_Status`
- `PAY_0` → `Pay_Status_April`
- …and more

This improves understanding for BI reports and stakeholders.

---

### **4. Data Cleaning**
- Removed duplicates  
- Handled incorrect categories  
- Converted numerical ranges into categorized bins  
- Converted month-over-month payment history into consistent format  
- Fixed outliers using percentile clipping  
- Ensured correct data types  

---

### **5. Exploratory Data Analysis (EDA)**
Studied:
- Default rates by Gender, Education, Marital Status  
- Payment delays and their contribution to default  
- Bill amount vs. default risk  
- Correlation heatmaps  
- Boxplots for understanding variability  
- Distribution analysis for skewed variables  

---

### **6. Feature Engineering**
Created model-ready features:
- Payment delay counts  
- Total bill amount  
- Total previous payments  
- Utilization ratio  
- Risk patterns in repayment history  

Removed irrelevant features for cleaner ML input.

---

### **7. Train–Test Split**
Split dataset into:
- **70% training**
- **30% testing**

Ensured balanced and representative data.

---

### **8. Model Training**
Trained two models:

#### ✔️ Random Forest Classifier  
- Good baseline  
- Handles imbalanced data  
- Robust to noise  

#### ✔️ XGBoost Classifier  
- Best performance  
- Handles complex interactions  
- Excellent for tabular data  

Hyperparameters were tuned for better performance.

---

### **9. Evaluation Metrics**
Evaluated using:
- **Accuracy**
- **F1 Score**
- **AUC Score**
- **Confusion Matrix**
- **Classification Report**

Created a comparison table to identify the best model.

---

### **10. Model Comparison**
| Model           | Accuracy | F1 Score | AUC |
|----------------|----------|----------|------|
| Random Forest  | x.xx     | x.xx     | x.xx |
| XGBoost        | x.xx     | x.xx     | x.xx |

👉 **XGBoost performed better** and was selected as the final model.

This is the **risk score** used for Power BI visualization.

Exported:
- **clean_data_with_prob.csv**
- **trained_model.pkl**

---

### **12. Power BI Dashboard**
Prepared dataset for Power BI to visualize:
- Default Risk by Age & Gender  
- Risk by Education Level & Marital Status  
- Risk by Payment Delay Patterns  
- High-risk customer segments  
- Risk score KPI cards  
- Distribution of risk across credit limits  

---

## 🛠 Tools & Technologies

### **Programming & ML**
- Python  
- Pandas, NumPy  
- Scikit-Learn  
- XGBoost  
- Matplotlib, Seaborn  

### **Business Intelligence**
- Power BI  

### **Version Control**
- Git  
- GitHub  

---

---

## 📊 Key Insights
- Customers with **payment delays ≥ 2 months** show sharply increasing default risk  
- Higher **credit utilization** strongly correlates with default  
- Risk is higher for certain education groups  
- Bill amount alone doesn't predict risk — **behavior patterns do**  
- Model identifies “silent risk” customers who appear normal but have subtle risk indicators  

---

## 💼 Business Impact
This project helps financial institutions:
- Reduce default rates  
- Improve loan approval strategy  
- Enable proactive customer engagement  
- Segment risk for better credit-line decisions  
- Build data-driven risk management frameworks  

---

## 🚀 Future Enhancements
- Add SHAP explainability visualizations  
- Deploy model via Flask/Streamlit  
- Automate data refreshing  
- Real-time scoring API  
- Enhanced BI monitoring dashboard  

---

## 🙌 Author
**Mazhar Khan**  
Data Analyst | Business Analytics  

📧 Email: *mazhark2028@gmail.com*  
🔗 LinkedIn: *www.linkedin.com/in/mazhar-khan-7a52a620a*  

---



---

### **11. Generate Default Probability**
Added a new scoring column:
