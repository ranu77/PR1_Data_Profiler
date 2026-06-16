# PR1_Data_Profiler

Data Preprocessing & Feature Engineering Project

Overview

This project focuses on the end-to-end data processing pipeline for a telecommunications customer dataset. The goal is to prepare raw data for machine learning by performing data acquisition, cleaning, and exploratory data analysis (EDA) to identify patterns that lead to customer churn.

Objectives
- Understand the data analysis workflow  
- Collect data from multiple sources (CSV, JSON, SQL, API)  
- Perform data cleaning and preprocessing  
- Conduct exploratory data analysis (EDA) using Seaborn  
- Generate automated data profiling report using YData Profiling  
- Identify factors influencing customer churn

Dataset Sources
CSV file 
JSON file 
SQL database
REST API 

Dataset Description
The dataset consists of 7,043 customer records containing demographic, service usage, and billing information:
Features: Tenure, Contract Type, Payment Method, Monthly Charges, Total Charges.
Target: Churn (Binary: Yes/No).

Technologies Used
Languages: Python (Jupyter Notebook)
Libraries: Pandas, NumPy, Seaborn, Matplotlib, YData Profiling, SQLite3.

Project Workflow

Part A: Fundamentals
- Introduction to Data Analysis  
- Data Science Project Lifecycle  
- Machine Learning Problem Statement (Customer Churn Prediction)  
- Tensor concepts with NumPy examples

Part B: Data Acquisition
Data was collected from one source and used in different format:
- CSV Files  
- JSON Files  
- SQLite Database  
- API

  <img width="1025" height="379" alt="image" src="https://github.com/user-attachments/assets/5e2a079c-9be8-4ccd-a494-816414d9666f" />

  <img width="1039" height="541" alt="image" src="https://github.com/user-attachments/assets/36485514-a4eb-467c-9d30-2671430faffb" />

  <img width="1019" height="522" alt="image" src="https://github.com/user-attachments/assets/60e4aa1a-7c21-4e31-8825-97d9bfa709b3" />

  <img width="1021" height="542" alt="image" src="https://github.com/user-attachments/assets/42dcb6b0-e1cc-4ff8-bdfb-35fa0affebc3" />

  All datasets were merged and prepared for analysis.

Part C: Data Understanding & Cleaning
-Diagnostic phase: Used .info() and .describe() to identify inconsistencies.
-Cleaning operations:
  Fixed TotalCharges type conversion (converted from object to float64).
  Imputed missing TotalCharges values using the median.
  Removed non-predictive features like customerID.
  Validated data integrity (duplicates = 0).

Part D: Exploratory Data Analysis (EDA)

-Univariate Analysis: Evaluated distributions of tenure, monthly charges, Total Charges.
(Note: The Telco Customer Churn dataset does not contain Age, Income, and Purchase columns. Therefore, equivalent variables available in the dataset were used for analysis:
Age - Tenure,
Income - MonthlyCharges,
Purchases - TotalCharges)
<img width="724" height="521" alt="image" src="https://github.com/user-attachments/assets/5361b7cd-a7ae-4e68-be79-e2c199a56ab6" />
<img width="716" height="520" alt="image" src="https://github.com/user-attachments/assets/b66bd1c5-bc14-4485-a25e-e955fb4824e4" />
<img width="710" height="506" alt="image" src="https://github.com/user-attachments/assets/ab98690c-56be-4617-852e-960f07757dd1" />


-Bivariate Analysis: Investigated the relationship between churn and contract types (Month-to-month vs. Long-term).
(Note: The Telco Customer Churn dataset does not contain Purchases. Therefore, equivalent variable available in the dataset were used for analysis:
Purchases - Churn)
<img width="715" height="511" alt="image" src="https://github.com/user-attachments/assets/95340113-3665-47c0-9634-0e8f34ac302e" />


(Note: The Telco Customer Churn dataset does not contain Income. Therefore, equivalent variable available in the dataset were used for analysis:
Income - Monthly Charges)
<img width="704" height="528" alt="image" src="https://github.com/user-attachments/assets/189ec69e-cc49-4916-97e6-55f07df9f3d9" />


-Multivariate Analysis: Generated a correlation matrix to confirm the strong relationship between tenure and TotalCharges.
<img width="724" height="511" alt="image" src="https://github.com/user-attachments/assets/3d90c40e-8f07-4c4b-929b-253d5631df8f" />
<img width="567" height="512" alt="image" src="https://github.com/user-attachments/assets/6c1e80f0-e5b9-4a0b-84b6-b2fa0f2ae2a9" />

Part E: Data Profiling
-Generated Telco_Profiling_Report.html using YData Profiling.
-Identified key statistical warnings and data distributions that justify the selected preprocessing steps.

<img width="937" height="528" alt="image" src="https://github.com/user-attachments/assets/3374e7f8-0486-4112-9741-a6a499f3822a" />

Generated Files
-data_profiler.ipynb
-Telco_Profiling_Report.html

Key Findings
Churn Drivers: Analysis reveals that customers with month-to-month contracts exhibit significantly higher churn rates.
Data Quality: The cleaning process successfully rectified type-mismatch errors in financial columns, ensuring the dataset is now "ML-Ready."
Feature Correlation: A clear positive correlation exists between customer tenure and total charges, indicating the importance of long-term retention.
  
Conclusion
This project demonstrates the transition from raw, multi-source data to a structured analytical format. The insights gained—specifically regarding contract types and tenure—provide a data-driven basis for future customer retention modeling.


 



