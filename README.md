# Supermarket Sales Analysis Project

## Overview

This repository contains a complete data analysis pipeline for supermarket sales data. The project covers data preprocessing, exploratory data analysis (EDA), SQL querying, feature engineering, visualization, and machine-learning-ready encoding. The goal is to extract business insights across branches, customers, product lines, payment methods, and temporal trends.

This work was developed as part of a data analysis assignment.

---

## Project Structure

```
supermarket-sales-analysis/
│
├── supermarket_sales.csv               # Original dataset
├── modified_supermarket_sales.csv      # Cleaned and processed dataset
├── supermarket_sales.db                # SQLite database
│
├── supermarket_analysis.ipynb          # Main analysis notebook
├── Dashboard.pbix                      # Main power bi dashboard
│
├── README.md                           # Project documentation
└── requirements.txt                    # Package dependencies
```

---

## Technologies Used

**Programming & Libraries**

* Python 3.x
* Pandas – Data manipulation
* NumPy – Numerical computations
* Matplotlib & Seaborn – Visualizations
* SQLite3 – Database operations
* Scikit-learn – Label encoding for ML

---

## Data Processing Workflow

### 1. Data Loading

* Imported CSV file
* Explored dataset using `.head()`, `.info()`, `.describe()`

### 2. Data Cleaning

* Renamed inconsistent columns
* Checked for missing values
* Validated data types

### 3. Feature Engineering

* Converted date and time into:

  * Year, Month, Day
  * Weekday
  * Hour
* Created `Avg_price_per_unit = Total / Quantity`
* Mapped Branch codes → City names (A = Naypyitaw, B = Yangon, C = Mandalay)

### 4. Data Export

* Saved cleaned dataset
* Loaded the modified dataset into an SQLite database (`Market` table)

---

## Visualizations Included

The notebook contains a wide range of visual insights:

### Sales & Branch Analysis

* Invoice count per branch
* Total sales by city
* Product line distribution by city

### Customer Behavior

* Purchases by gender
* Customer type distribution
* Gross income by gender (boxplot)

### Product Line Analysis

* Sales per product line
* Rating distributions (KDE / violin plots)

### Time-Based Patterns

* Hourly transaction count
* Transaction trends by hour
* Weekday-based patterns

### Payment Insights

* Payment method usage per branch
* Heatmaps of payment distribution

All plots are generated using Matplotlib and Seaborn.

---

## SQL Analysis

An SQLite database was created for query-based insights.

### Included SQL Queries

* High-value transactions (Total > 1000)
* Total revenue by city
* Payment method frequency by branch
* Quantity sold per product line
* Transaction counts by customer type
* Rating aggregation by branch

The SQL component demonstrates relational analysis and data validation.

---

## Machine Learning Preparation

Categorical columns encoded using **LabelEncoder**:

* Gender
* Customer_type
* Payment
* Product_line
* Branch
* City
* Weekday

This prepares the dataset for potential ML models such as:

* Sales prediction
* Customer segmentation
* Product line forecasting

---

## Power BI Dashboard

A Power BI dashboard accompanies the project for interactive analysis.

**Dashboard Link:**
The dashboard is available through Power BI (access may require permission).

---

## Key Findings

The analysis reveals important business insights:

* City B (Yangon) generally exhibits the highest sales volume.
* Female customers tend to provide slightly higher ratings.
* Health & Beauty and Food & Beverages are among the top-performing product lines.
* Member customers usually spend more than Normal customers.
* Payment preferences vary significantly between branches.
* Sales peak between 13:00 and 16:00 across all locations.

---

## How to Run

### 1. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 2. Open the Jupyter Notebook

Run the main analysis file:

```bash
jupyter notebook supermarket_analysis.ipynb
```

### 3. Ensure dataset paths are correct

Place the CSV file in the project directory or update paths in the notebook.

---

## Future Enhancements

Planned improvements include:

* Adding Linear Regression or Random Forest for sales prediction
* Automating weekly report generation
* Integrating live dashboards
* Advanced segmentation (e.g., RFM analysis)
* Time-series forecasting using ARIMA or Prophet

---

## License

This project is provided for academic and educational purposes.

