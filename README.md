<img width="1359" height="616" alt="Screenshot from 2026-06-13 14-25-22" src="https://github.com/user-attachments/assets/91c1ec39-493d-4ed7-9c07-5013d64f57c3" />
<img width="593" height="310" alt="Screenshot from 2026-06-13 15-04-51" src="https://github.com/user-attachments/assets/c4b32a58-3ddc-4451-8a5b-d1d4430d97ba" />Sales & Demand Forecasting for Businesses

Future Interns – Machine Learning Internship (Task 1)

Project Overview

This project focuses on forecasting future sales using historical retail transaction data. The objective is to help businesses estimate future demand, improve inventory management, and support data-driven decision-making.

Dataset

Dataset: Online Retail Dataset

The dataset contains:

Invoice details
Product information
Quantity sold
Unit price
Customer information
Transaction date and time
Project Workflow
1. Data Preprocessing
Loaded and explored the dataset
Removed invalid and missing values
Converted date columns into datetime format
Created a Sales column:
Sales = Quantity * UnitPrice
2. Daily Sales Aggregation

Transaction-level data was aggregated into daily sales totals to create a time-series forecasting dataset.

3. Feature Engineering

The following features were created:

Year
Month
Day
DayOfWeek
Lag1 (Previous Day Sales)
Lag7 (Sales from Previous Week)
Rolling7 (7-Day Moving Average)

These features help the model learn historical sales patterns.

Models Used
Linear Regression

Used as a baseline forecasting model.

Random Forest Regressor

Used to capture non-linear relationships in sales data.

Model Evaluation
Model	MAE	R² Score
Linear Regression	12676.39	0.4764
Random Forest Regressor	14994.91	0.2383
Best Model

Linear Regression achieved the lowest prediction error and highest R² score, making it the best-performing model for this dataset.

Visualizations
Sales Distribution
Distribution of daily sales values.
Actual vs Predicted Sales
Comparison between actual sales and model predictions.
Model Performance Analysis
Evaluation using MAE and R² metrics.

(Add screenshots in the repository and link them here.)

Business Insights
Historical sales trends significantly influence future demand.
Lag-based features improved forecasting performance.
Moving averages helped capture short-term sales patterns.
The model can support inventory planning and demand forecasting.
Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
Jupyter Notebook
Repository Structure
FUTURE_ML_01/
│
├── sales_forecasting.ipynb
├── README.md
├── requirements.txt
└── images/
Future Improvements
Use advanced time-series models such as ARIMA or Prophet.
Incorporate holiday and seasonal features.
Deploy the model as a web application for business use.
Internship Information

Organization: Future Interns
Track: Machine Learning
Task: Sales & Demand Forecasting for Businesses
Repository: FUTURE_ML_01

