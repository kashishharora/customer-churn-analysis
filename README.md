# 📊 Customer Churn Prediction

Predicting customer churn for a Telecom company using Exploratory Data Analysis and Machine Learning.

---

## 📁 Dataset

- **Source:** [Telco Customer Churn - Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Rows:** 7,043 customers
- **Columns:** 21 

---

## 🔧 Steps Performed

### 1. Data Cleaning
- Dropped `customerID` (not useful)
- Converted `TotalCharges` to numeric
- Dropped rows where `tenure = 0` (no activity)
- Handled all null values

### 2. Exploratory Data Analysis (EDA)
- Plotted every feature against Churn using Seaborn
- Used percentage crosstabs for clear comparison
- Used Violin and Box plots for numerical features
- Correlation Heatmap to find feature relationships
- Log Transformation on skewed columns

### 3. Key Insights Found
| Feature | Insight |
|---|---|
| Senior Citizens | 41.6% churn vs 23.6% for non-seniors |
| Contract Type | Monthly = 42.7% churn, Two-year = only 2.8% |
| Internet Service | Fiber optic users churn 41.8% |
| Payment Method | Electronic check users churn 45.2% |
| Tenure | Low tenure customers churn more |
| Online Security | No security = 41.7% churn |

### 4. Model Training
Three ML models trained with class balancing:
- Logistic Regression
- Random Forest
- CatBoost

### 5. Model Results
| Model | Accuracy | ROC-AUC |
|---|---|---|
| Logistic Regression | 72.9% | 0.841 |
| Random Forest | 78.6% | 0.817 |
| CatBoost | 79.1% | 0.835 |

---

## 🛠️ Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- CatBoost


