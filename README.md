# Sales & Demand Forecasting for Businesses

## Future Interns - Machine Learning Internship (Task 1)

### Project Overview

Accurate sales forecasting is essential for inventory planning, demand management, and strategic business decision-making. This project develops a machine learning-based forecasting system that predicts future sales using historical retail transaction data.

The workflow includes data preprocessing, feature engineering, exploratory data analysis, model development, performance evaluation, and business insight generation.

---

## Objective

The primary objective of this project is to forecast future business sales using historical transaction records and evaluate the effectiveness of different machine learning models for demand prediction.

---

## Dataset

**Dataset Used:** Online Retail Dataset

The dataset contains transactional information including:

* Invoice Number
* Product Details
* Quantity Purchased
* Unit Price
* Customer Information
* Transaction Date and Time
* Country

---

## Data Preprocessing

The following preprocessing steps were performed:

* Loaded and inspected the dataset
* Removed missing and invalid records
* Converted transaction timestamps into datetime format
* Created a new Sales feature:

```python
Sales = Quantity * UnitPrice
```

* Aggregated transaction-level records into daily sales values

---

## Feature Engineering

To improve forecasting performance, several time-series features were generated:

| Feature   | Description              |
| --------- | ------------------------ |
| Year      | Transaction Year         |
| Month     | Transaction Month        |
| Day       | Day of Month             |
| DayOfWeek | Weekday Indicator        |
| Lag1      | Previous Day Sales       |
| Lag7      | Sales from Previous Week |
| Rolling7  | 7-Day Moving Average     |

These features help the model capture temporal patterns and historical sales behavior.

---

## Exploratory Data Analysis

The sales data was analyzed to understand:

* Daily sales distribution
* Sales variability
* Historical trends
* Demand fluctuations

Visualizations were created using Matplotlib and Seaborn to identify patterns and support model development.

---

## Machine Learning Models

Two machine learning models were implemented and compared:

### 1. Linear Regression

A baseline regression model used to establish a forecasting benchmark.

### 2. Random Forest Regressor

An ensemble learning model capable of capturing non-linear relationships in sales data.

---

## Model Evaluation

Performance was evaluated using:

### Mean Absolute Error (MAE)

Measures the average absolute difference between actual and predicted sales.

### R² Score

Measures how well the model explains the variability in sales data.

| Model                   |       MAE | R² Score |
| ----------------------- | --------: | -------: |
| Linear Regression       | 12,676.39 |   0.4764 |
| Random Forest Regressor | 14,994.91 |   0.2383 |

---

## Results

Linear Regression achieved the best overall performance with:

* Lower prediction error
* Higher explanatory power
* Better generalization on the test dataset

Therefore, Linear Regression was selected as the final forecasting model for this project.

---

## Business Insights

Key observations obtained from the analysis include:

* Historical sales significantly influence future demand.
* Lag-based features improved forecasting performance.
* Weekly sales patterns contribute to demand prediction.
* Rolling averages help smooth short-term fluctuations.
* Forecasting models can support inventory planning and stock management.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Jupyter Notebook

---

## Project Structure

```text
FUTURE_ML_01/
│
├── data/
│   └── Online Retail.xlsx
│
├── notebooks/
│   └── sales_forecasting.ipynb
│
├── images/
│   ├── sales_distribution.png
│   ├── actual_vs_predicted.png
│   └── model_comparison.png
│
├── README.md
└── requirements.txt
```

---

## Future Improvements

Potential enhancements include:

* Implementation of ARIMA and Prophet forecasting models
* Hyperparameter optimization
* Seasonal decomposition analysis
* Holiday and event-based feature engineering
* Deployment as an interactive forecasting dashboard

---

## Internship Information

Organization: Future Interns

Track: Machine Learning

Task: Sales & Demand Forecasting for Businesses

Repository: FUTURE_ML_01

---

### Author

Machine Learning Intern | Future Interns

This project was completed as part of the Future Interns Machine Learning Internship Program to develop practical forecasting and predictive analytics skills using real-world business data.
