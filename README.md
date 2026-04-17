# Customer Churn Analysis
## Objective
### To analyze customer behavior and identify key factors contributing to customer churn in the telecom industry.
# About the Project
### Customer churn is one of the biggest challenges for any subscription-based business.
### This project analyzes real telecom customer data to answer:
### Why are customers leaving?
#### Which customers are most at risk?
#### What factors keep customers loyal?
#### What actions can a business take to reduce churn?
## This analysis reflects real work done by data analysts in product, growth, and retention teams.
## 📁 Dataset
#### Detail
#### Name: Telco Customer Churn Dataset 
#### Source:[Kaggle — IBM Watson Analytics](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) 
#### Records: 7,043 customers 
#### Features: 21 columns 
#### Target Column: Churn (Yes / No) 
#### Features include: demographics, internet service, contract type,payment method, monthly charges, tenure, and add-on services.
## 🛠️ Tools and Libraries
#### Library | Purpose |
#### | Pandas | Data cleaning and manipulation |
#### | NumPy | Numerical operations and log transformation |
#### | Seaborn | Data visualization |
#### | Matplotlib | Figure sizing and plot layout |
## 🔄 Project Workflow

### 🧹 Step 1 — Data Cleaning
#### Dropped `customerID` column — not useful for analysis
#### Converted `TotalCharges` from object to numeric using `pd.to_numeric(errors='coerce')`
#### Dropped rows where `tenure == 0` — customers with no activity
#### Verified null values after each cleaning step

### 📊 Step 2 — Exploratory Data Analysis (EDA)
#### Analyzed churn patterns across every feature:
#### Demographics — gender, senior citizen, partner, dependents
#### Services — phone, internet, online security, tech support, streaming
#### Billing — contract type, payment method, paperless billing
#### Numeric — monthly charges, total charges, tenure

## 💡 Key Insights

## Customer Segment Churn Rate 
#### Month-to-month contract-42% 
#### Two-year contract-3% 
#### Fiber optic internet-42% 
#### Electronic check payment-45% 
#### No online security-41% 
#### No tech support-41% 
#### Senior citizens-41% 
#### Customers with dependents-15% 
#### Low tenure (0–12 months)-50% 

## Business Recommendations

#### 1. Offer first-year discounts to convert month-to-month users to annual contracts
#### 2. Bundle online security and tech support for all new customers
#### 3. Investigate fiber optic service quality — high price but highest churn
#### 4. Build dedicated retention programs for senior citizens
#### 5. Focus onboarding and engagement in the first 12 months
#### 6. Incentivize customers to switch from electronic check to auto-pay

## 📊 Visualizations Used

#### Plot AND Purpose
##### sns.countplot: Churn count across all categorical features 
##### sns.violinplot:Distribution of numeric features by churn 
##### sns.boxplot:Outlier detection in TotalCharges 
##### sns.kdeplot:Distribution shape after log transformation 
##### sns.heatmap:Correlation matrix across all features 
