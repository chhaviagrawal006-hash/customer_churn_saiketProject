# 📊 Customer Churn Analysis and Prediction | Power BI

An interactive Power BI dashboard developed to analyze telecom customer churn, identify churn patterns across different customer segments, and provide insights that can support customer retention analysis.

---

## 📌 Project Overview

Customer churn is an important challenge for telecommunications companies because losing existing customers can affect revenue and long-term business growth.

This project uses the **Telco Customer Churn dataset** to analyze customer behavior and churn patterns using **Power BI, Power Query, and DAX**.

The dashboard provides an interactive view of:

- Overall customer churn
- Customer demographics
- Customer tenure
- Contract type
- Payment method
- Internet service
- Customer retention

> **Note:** The current project focuses on descriptive and diagnostic churn analysis using Power BI. A machine-learning prediction model is considered a future extension.

---

## 🎯 Objectives

The main objectives of this project are:

- Import and connect the telecom churn dataset to Power BI.
- Clean and transform the data using Power Query.
- Create meaningful DAX measures and KPIs.
- Analyze the overall customer churn rate.
- Analyze customer demographics.
- Analyze customer tenure and its relationship with churn.
- Compare churn across different contract types.
- Compare churn across payment methods.
- Compare churn across internet service types.
- Build an interactive dashboard using slicers.
- Generate insights that can support customer retention analysis.

---

## 🛠️ Tools & Technologies

| Tool / Technology | Purpose |
|---|---|
| **Power BI Desktop** | Dashboard development and visualization |
| **Power Query** | Data cleaning and transformation |
| **DAX** | KPI and calculated measure creation |
| **CSV** | Dataset format |
| **Data Visualization** | Customer churn analysis |

---

## 📂 Dataset

The project uses the **Telco Customer Churn dataset** containing customer-level information related to demographics, services, billing, tenure, and churn status.

### Important columns used

- `customerID`
- `gender`
- `SeniorCitizen`
- `Partner`
- `Dependents`
- `tenure`
- `InternetService`
- `Contract`
- `PaymentMethod`
- `MonthlyCharges`
- `TotalCharges`
- `Churn`

### Target Variable

The `Churn` column indicates whether a customer has left the telecom service:

- `Yes` → Customer churned
- `No` → Customer retained

---

## 🧹 Data Cleaning & Transformation

The data was prepared using **Power Query** before creating the dashboard.

The main preprocessing steps included:

1. Importing the CSV dataset into Power BI.
2. Checking and correcting column data types.
3. Converting `TotalCharges` into a numeric field.
4. Handling blank values in `TotalCharges`.
5. Checking customer records and duplicates.
6. Preparing fields for visualization.
7. Creating customer tenure groups.

### Customer Tenure Groups

Customer tenure was grouped into five categories:

| Tenure | Group |
|---|---|
| Up to 12 months | 0-12 Months |
| 13-24 months | 13-24 Months |
| 25-48 months | 25-48 Months |
| 49-60 months | 49-60 Months |
| 61-72 months | 61-72 Months |

This grouping makes the tenure distribution easier to visualize and interpret.

---

# 📐 DAX Measures

The dashboard uses DAX measures to calculate important KPIs.

### Total Customers

```DAX
Total Customers =
COUNTROWS('Telco_churn')
