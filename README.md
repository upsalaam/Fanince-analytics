# Finance Analytics Project

A complete **Finance Analytics project** built using **Excel, SQL
Server, and Power BI** to clean, analyze, and visualize business
transaction data.

The project follows a practical data analytics workflow:

**Excel → Data Cleaning → SQL Analysis → Power BI Dashboard → Business
Insights**

------------------------------------------------------------------------

## 📌 Project Overview

This project analyzes business financial transactions across multiple
branches, departments, categories, payment methods, and customer types.

The goal is to transform raw transaction data into useful financial
insights that can support business reporting and decision-making.

The project was developed as a portfolio project to demonstrate
practical skills in:

-   Data cleaning and preparation
-   SQL database creation and querying
-   Financial analysis
-   KPI development
-   Data visualization
-   Business insight generation
-   Power BI dashboard design

------------------------------------------------------------------------

## 🛠️ Tools & Technologies

  -----------------------------------------------------------------------
  Tool                                Purpose
  ----------------------------------- -----------------------------------
  **Microsoft Excel**                 Data cleaning, validation, and
                                      preparation

  **SQL Server**                      Database creation, data storage,
                                      and analysis

  **Power BI**                        Data modeling, DAX calculations,
                                      visualization, and dashboard
                                      development
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 📂 Project Structure

``` text
Finance-Analytics-Project/
│
├── Excel/
│   └── Business Analysis.xlsx
│
├── SQL/
│   └── SQLQuery finance project.sql
│
├── PowerBI/
│   └── Finance Analytics Dashboard.pbix
│
├── Screenshots/
│   ├── Finance Analytics Dashboard.png
│   └── Expense Analysis.png
│
└── README.md
```

------------------------------------------------------------------------

# 1. 📊 Excel --- Data Cleaning & Preparation

The original Excel workbook contains a **raw transaction dataset** and a
cleaned version prepared for analysis.

### Raw Data

-   **670 transaction rows**
-   15 core business fields
-   Included missing values, duplicate transaction IDs, inconsistent
    payment-method values, and numerical anomalies.

### Data Cleaning

The cleaned dataset contains **650 transaction rows** after removing
duplicate transaction records and addressing missing/inconsistent
values.

Key cleaning activities included:

-   Removing duplicate `Transaction_ID` records
-   Handling missing values
-   Standardizing categorical values
-   Checking date consistency
-   Reviewing numerical fields
-   Checking quantity, revenue, expense, unit price, and total amount
-   Preparing columns for analysis
-   Validating transaction fields before loading the data into the
    analytical workflow

### Main Fields

``` text
Transaction_ID
Date
Branch
Department
Category
Description
Revenue
Expense
Payment_Method
Customer_Type
Employee_ID
Quantity
Unit_Price
Total_Amount
Status
```

### Business Dimensions

The cleaned dataset covers:

-   **5 Branches:** Mogadishu, Kismayo, Hargeisa, Garowe, Baydhabo
-   **4 Departments:** Sales, Operations, Administration, Logistics
-   **5 Categories:** Electronics, Household, Office Supplies, Clothing,
    Food & Beverage
-   **4 Customer Types:** Individual, Business, NGO, Government
-   **3 Transaction Statuses:** Paid, Pending, Cancelled
-   Multiple payment methods including EVC Plus, Zaad, Sahal, Cash, and
    Bank Transfer

------------------------------------------------------------------------

# 2. 🗄️ SQL Server --- Database & Analysis

The SQL component creates a dedicated database and a structured
transaction table.

### Database

``` sql
CREATE DATABASE SOMALI_BUSSINES
```

### Main Table

``` text
BusinessTransactions
```

The table was designed with appropriate data types for:

-   Transaction identifiers
-   Dates
-   Branches and departments
-   Financial values
-   Payment methods
-   Customer types
-   Quantities and unit prices
-   Transaction status

### SQL Skills Demonstrated

The SQL work demonstrates practical database and analytical skills such
as:

-   Database creation
-   Table creation
-   Primary key definition
-   Data insertion
-   Data type selection
-   Financial field handling
-   Structured transaction analysis

The SQL dataset contains the cleaned business transaction records used
for the analytical workflow.

------------------------------------------------------------------------

# 3. 📈 Power BI --- Finance Analytics Dashboard

The Power BI dashboard consists of **two analytical pages**, each with a
different purpose.

------------------------------------------------------------------------

## Page 1 --- Finance Analytics Dashboard

The first page provides an executive-level view of the financial
performance of the business.

### Key KPIs

-   **Total Revenue:** 293.06K
-   **Total Expense:** 185.34K
-   **Net Profit:** 107.72K
-   **Profit Margin:** 36.76%

### Visual Analysis

The page includes:

-   Revenue by Branch
-   Expense by Customer Type
-   Profit Margin by Branch
-   Net Profit by Branch
-   Monthly Revenue Trend
-   Expense by Department

### Main Purpose

This page answers questions such as:

-   How much revenue was generated?
-   How much was spent?
-   What is the resulting net profit?
-   What is the overall profit margin?
-   Which branches generate the most revenue?
-   How does profitability differ between branches?
-   How does revenue change over time?
-   Which departments account for the largest expenses?

------------------------------------------------------------------------

## Page 2 --- Expense Analysis

The second page focuses specifically on **expense behavior and
distribution**.

### Key KPIs

-   **Average Expense:** 285.13
-   **Highest Expense Category:** Electronics
-   **Highest Expense Branch:** Mogadishu

### Visual Analysis

The page includes:

-   Monthly Expense Trend
-   Expense by Description
-   Expense by Category
-   Expense by Status
-   Expense by Branch
-   Expense by Payment Method

### Main Purpose

This page answers questions such as:

-   How are expenses changing over time?
-   Which expense categories account for the largest amounts?
-   Which branch has the highest expense?
-   Which descriptions contribute most to expenses?
-   How are expenses distributed by transaction status?
-   Which payment methods are used most for expenses?

------------------------------------------------------------------------

# 📐 Power BI Measures

The dashboard uses calculated measures to generate financial KPIs and
analytical metrics.

Examples include:

``` dax
Total Revenue = SUM('Data cleanin'[Revenue])
```

``` dax
Total Expense = SUM('Data cleanin'[Expense])
```

``` dax
Net Profit = [Total Revenue] - [Total Expense]
```

``` dax
Profit Margin = DIVIDE([Net Profit], [Total Revenue], 0)
```

Additional measures were created for expense analysis, averages,
branch/category comparisons, and dashboard KPIs.

------------------------------------------------------------------------

# 🔎 Key Business Insights

The dashboard highlights several patterns in the dataset:

1.  **Revenue exceeds total expense**, resulting in a positive net
    profit in the Power BI model.
2.  **Mogadishu** records the highest revenue among the branches shown
    on the dashboard.
3.  **Mogadishu** also records the highest expense in the expense
    analysis.
4.  **Electronics** is the highest expense category in the dashboard.
5.  **Sales** represents the largest department by expense.
6.  **Zaad** accounts for the largest expense amount among the payment
    methods shown.
7.  Monthly revenue and expense trends show noticeable variation across
    the year.

These insights are descriptive findings from the project data and are
intended to demonstrate how a dashboard can support financial
monitoring.

------------------------------------------------------------------------

# 🔄 End-to-End Workflow

``` text
Raw Excel Data
      ↓
Data Cleaning & Validation
      ↓
Cleaned Excel Dataset
      ↓
SQL Server Database
      ↓
SQL Analysis
      ↓
Power BI Data Model
      ↓
DAX Measures
      ↓
Interactive Dashboard
      ↓
Financial Insights
```

------------------------------------------------------------------------

# 🎯 Business Questions Addressed

This project was designed around practical financial questions:

### Revenue & Profitability

-   What is the total revenue?
-   What is the total expense?
-   What is the net profit?
-   What is the profit margin?
-   Which branches generate the most revenue?
-   Which branches generate the most profit?

### Expense Management

-   Which category has the highest expense?
-   Which branch has the highest expense?
-   Which department has the largest expense?
-   What is the monthly expense trend?
-   Which payment method represents the highest expense?
-   How are expenses distributed by status?

### Customer & Operations

-   How does expense vary by customer type?
-   Which departments contribute most to business expenses?
-   How do transaction patterns change over time?

------------------------------------------------------------------------

# 📸 Dashboard Preview

### Page 1 --- Finance Analytics Dashboard

![Finance Analytics
Dashboard](Screenshots/Finance%20Analytics%20Dashboard.png)

### Page 2 --- Expense Analysis

![Expense Analysis](Screenshots/Expense%20Analysis.png)

------------------------------------------------------------------------

# 💡 What This Project Demonstrates

This project demonstrates the ability to move from **raw business data
to a finished analytical product**.

### Excel

-   Data cleaning
-   Duplicate detection and removal
-   Missing-value handling
-   Data validation
-   Data preparation

### SQL

-   Database creation
-   Relational table design
-   Primary keys
-   Data insertion
-   Structured financial data handling

### Power BI

-   Data modeling
-   DAX measures
-   KPI cards
-   Interactive filtering
-   Trend analysis
-   Category and branch analysis
-   Financial dashboard design
-   Business insight presentation

------------------------------------------------------------------------

# 🚀 Future Improvements

Possible future improvements include:

-   Adding a dedicated date/calendar table
-   Adding year-over-year financial comparisons
-   Adding budget vs. actual analysis
-   Adding variance analysis
-   Adding drill-through pages for branch-level investigation
-   Adding more advanced DAX measures
-   Automating the data-refresh process
-   Connecting Power BI directly to SQL Server

------------------------------------------------------------------------

# 👤 Author

**Abdisalaam Hassan**

Data Analytics Portfolio Project

**Skills demonstrated:**\
`Excel` · `SQL Server` · `Power BI` · `DAX` · `Data Cleaning` ·
`Data Visualization` · `Business Analysis`

------------------------------------------------------------------------

## ⭐ Project Summary

**Finance Analytics** is an end-to-end data analytics project that
demonstrates how raw financial transaction data can be cleaned in Excel,
structured and analyzed with SQL Server, and transformed into an
interactive Power BI dashboard for financial reporting and business
analysis.
