![Meddybuddy Banner](assets/github_banner.png)

#  Insurance Cost Analysis & Prediction  
### MediBuddy Case Study | End-to-End Data Analytics & Machine Learning Project

##  Overview
This project simulates a real-world insurance analytics use case for a digital healthcare
platform like MediBuddy. The objective is to analyze customer demographics, health,
and lifestyle factors to identify key drivers of insurance costs and build a machine
learning model to predict insurance charges.

The project follows an industry-style workflow, combining exploratory data analysis,
statistical validation, risk segmentation, machine learning, and business insights.

---

##  Business Objectives
- Identify factors that significantly impact insurance claim amounts
- Evaluate whether demographic attributes should constrain policy issuance
- Analyze the impact of health indicators such as BMI and smoking
- Segment customers into risk categories for underwriting decisions
- Build a predictive model to estimate insurance cost before policy approval

---

##  Dataset Description
Two datasets were used and later merged:

### 1️⃣ Personal Details Dataset
- Age  
- Gender  
- Region  
- Number of dependents  
- Smoking status  

### 2️⃣ Insurance & Health Dataset
- Body Mass Index (BMI)  
- Insurance charges (target variable)

After cleaning and preprocessing, a unified dataset was created for analysis and modeling.

---

##  Data Preparation & Feature Engineering
- Verified data types, missing values, and duplicates
- Standardized categorical values
- Created BMI categories (underweight, normal, overweight, obese)
- Prepared clean, analysis-ready data
- Saved final cleaned dataset for reproducibility

---

##  Exploratory Data Analysis (EDA)
Key insights discovered:
- Smoking is the strongest lifestyle-related cost driver
- Higher BMI and increasing age significantly increase insurance costs
- Gender shows minimal impact on insurance charges
- Dependents and region have a moderate influence

EDA was supported by visual analysis and statistical testing.

---

##  Risk Segmentation
Customers were segmented into **Low, Medium, and High Risk** categories using
data-driven charge thresholds:

- Low Risk: ≤ median insurance charge  
- Medium Risk: median to 75th percentile  
- High Risk: > 75th percentile  

### Validation
Risk segments were validated against:
- Smoking status
- BMI category
- Average age

High-risk customers showed a higher concentration of smokers, obese BMI categories,
and older individuals, confirming meaningful risk separation.

---

##  Machine Learning Approach
### Modeling Pipeline
- Train–test split
- Preprocessing pipeline:
  - Standard scaling for numerical features
  - One-hot encoding for categorical features
- Models evaluated:
  - Linear Regression (baseline)
  - Random Forest Regressor
  - Gradient Boosting Regressor

### Model Selection
- Hyperparameter tuning using GridSearchCV
- Evaluation metrics:
  - RMSE
  - R² score
    

The final model demonstrated strong predictive performance and generalization.

---

##  Model Explainability
Feature importance analysis showed:
- BMI and age as the strongest numerical predictors
- Number of dependents with moderate impact
- Smoking, gender, and region contributing less due to binary/categorical nature

Model behavior aligned well with EDA and statistical findings, reinforcing trust
in predictions.

---

##  Error Analysis
- The model slightly underpredicts extreme high-cost cases
- This behavior is expected due to:
  - Heavy-tailed insurance cost distribution
  - Limited dataset size (~1,400 records)
- Predictions remain reliable for the majority of customers

This reflects realistic challenges in insurance analytics.

---

##  Example Prediction
The trained model can be used to predict insurance cost for a new customer by
providing demographic, health, and lifestyle details. This supports proactive
pricing and underwriting decisions before policy issuance.

---

##  Key Business Insights
- Smoking should be a primary pricing factor
- BMI and age should significantly influence premiums
- Gender should not restrict policy issuance
- Region-based pricing adjustments may be explored
- Wellness-based incentives can reduce long-term claim costs

---

##  Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- SciPy
- Jupyter Notebook


