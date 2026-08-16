# 📡 Telecom Customer Churn — Data Profiling Project
### Data Acquisition, Cleaning & Exploratory Data Analysis | Data Preprocessing & Feature Engineering

---

## 📌 Project Overview

An end-to-end data preprocessing pipeline built for a telecommunications customer dataset. The project covers data acquisition from multiple sources, data cleaning, exploratory data analysis (EDA), and automated data profiling — all aimed at preparing raw data for machine learning to predict customer churn.

---

## 🎯 Objectives

- Understand the full data analysis workflow and project lifecycle
- Collect and merge data from multiple sources (CSV, JSON, SQL, API)
- Clean and preprocess raw data for ML readiness
- Conduct exploratory data analysis (EDA) using Seaborn
- Generate an automated data profiling report using YData Profiling
- Identify key factors influencing customer churn

---

## 🗂️ Dataset

| Property | Details |
|---|---|
| Records | 7,043 customers |
| Domain | Telecommunications |
| Target Variable | `Churn` (Yes / No) |
| Key Features | Tenure, Contract Type, Payment Method, Monthly Charges, Total Charges |

**Data Sources:**
- CSV file
- JSON file
- SQLite database
- REST API

All four sources contained the same dataset in different formats and were merged for analysis.

---

## 🔄 Project Workflow

### Part A — Fundamentals
- Introduction to Data Analysis and the Data Science Project Lifecycle
- Machine Learning Problem Statement: Customer Churn Prediction
- Tensor concepts with NumPy examples

---

### Part B — Data Acquisition
Data was collected from four different format sources and merged into a single unified dataset:

- CSV → loaded with Pandas
- JSON → parsed and normalized
- SQLite → queried using SQLite3
- REST API → fetched and integrated

---

### Part C — Data Understanding & Cleaning

**Diagnostic phase:**
- Used `.info()` and `.describe()` to identify inconsistencies

**Cleaning operations:**
- Fixed `TotalCharges` type conversion — from `object` to `float64`
- Imputed missing `TotalCharges` values using median
- Removed non-predictive feature `customerID`
- Validated data integrity — duplicates confirmed as 0

---

### Part D — Exploratory Data Analysis (EDA)

**Univariate Analysis:**
Evaluated distributions of Tenure, Monthly Charges, and Total Charges

*(Note: Telco dataset does not contain Age, Income, or Purchase columns — equivalent variables were used: Age → Tenure, Income → MonthlyCharges, Purchases → TotalCharges)*

**Bivariate Analysis:**
- Investigated relationship between Churn and Contract Type (Month-to-month vs Long-term)
- Analyzed Monthly Charges distribution across churned vs retained customers

**Multivariate Analysis:**
- Generated a correlation matrix confirming strong positive relationship between Tenure and TotalCharges

---

### Part E — Data Profiling
- Generated `Telco_Profiling_Report.html` using YData Profiling
- Identified key statistical warnings and data distributions
- Used findings to justify selected preprocessing steps

---

## 📊 Key Findings

| Finding | Insight |
|---|---|
| Churn Driver | Customers on month-to-month contracts show significantly higher churn rates |
| Data Quality | Type-mismatch in `TotalCharges` fixed — dataset is now ML-ready |
| Feature Correlation | Strong positive correlation between tenure and total charges — long-term retention is critical |

---

## 📁 Repository Structure

```
data-profiling-project/
│
├── data_profiler.ipynb            # Full Jupyter Notebook — all parts A to E
└── Telco_Profiling_Report.html    # Automated YData Profiling report
```

---

## 💻 Tools & Libraries Used

- Python (Jupyter Notebook)
- Pandas, NumPy
- Seaborn, Matplotlib
- YData Profiling
- SQLite3

---

## 🚀 How to Run

1. Clone the repository
2. Open `data_profiler.ipynb` in Jupyter Notebook or Google Colab
3. Run all cells from top to bottom
4. Open `Telco_Profiling_Report.html` in any browser to view the profiling report

---

## ✅ Conclusion

This project demonstrates the full transition from raw, multi-source data to a structured, analysis-ready format. Key insights — particularly around contract types and customer tenure — provide a solid data-driven foundation for future churn prediction modeling.

---

## 👩‍💻 Author

**Devanshi Kanthariya**
