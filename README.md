# Customer-Sales-Performance-Analysis-Using-Data-Analytics


CHAPTER ONE: INTRODUCTION
1.1 Background of the Project
In today's business environment, organizations generate large amounts of sales data daily. However, raw data alone cannot support effective decision-making unless it is properly collected, cleaned, analyzed, and visualized.
This project focuses on analyzing sales transactions to discover important business insights such as sales trends, customer purchasing behaviour, product performance, and regional revenue distribution.
The project applies data analytics techniques using Excel, SQL, Python, and Power BI to transform raw sales data into meaningful information for business decisions.
1.2 Problem Statement
Many businesses struggle with:
Identifying their best-performing products
Understanding customer behaviour
Tracking revenue growth
Discovering weak-performing areas
Making decisions based on assumptions rather than data
This project solves these problems by analyzing sales data and presenting insights through interactive dashboards.
1.3 Aim of the Project
The aim of this project is to analyze customer sales data and develop a dashboard that helps management understand sales performance and improve decision-making.
1.4 Objectives
The objectives are:
To collect and prepare sales data for analysis.
To clean and transform raw data.
To analyze sales trends.
To identify top-performing products.
To study customer purchasing patterns.
To create an interactive business intelligence dashboard.
CHAPTER TWO: PROJECT REQUIREMENTS
Software Requirements
Software
Purpose
Microsoft Excel
Data cleaning
SQL
Database analysis
Python
Data processing
Power BI
Dashboard visualization
GitHub
Project documentation
CHAPTER THREE: DATASET DESCRIPTION
Dataset Name:
Sales_Data.csv
Sample data:
Order_ID
Date
Customer
Product
Category
Quantity
Price
Region
1001
01/01/2025
Ali Musa
Laptop
Electronics
2
350000
North
1002
03/01/2025
John Peter
Phone
Electronics
5
120000
South
1003
05/01/2025
Aisha Bello
Chair
Furniture
3
45000
West
CHAPTER FOUR: DATA CLEANING PROCESS
The following operations were performed:
1. Removing duplicates
Duplicate records were identified and removed.
2. Handling missing values
Empty fields were replaced or removed depending on importance.
3. Data formatting
Date fields were converted into proper date format.
4. Creating calculated columns
A new column was created:
Total Sales = Quantity × Unit Price
Example:
5 phones × ₦120,000
= ₦600,000
CHAPTER FIVE: DATA ANALYSIS USING SQL
Total Revenue
SELECT 
SUM(Quantity * Price) AS Total_Revenue
FROM Sales;
Best Selling Products
SELECT 
Product,
SUM(Quantity) AS Total_Sold
FROM Sales
GROUP BY Product
ORDER BY Total_Sold DESC;
Sales By Region
SELECT
Region,
SUM(Quantity * Price) AS Revenue
FROM Sales
GROUP BY Region;
Monthly Sales Trend
SELECT
MONTH(Date) AS Month,
SUM(Quantity * Price) AS Revenue
FROM Sales
GROUP BY MONTH(Date);
CHAPTER SIX: PYTHON DATA ANALYSIS
Libraries used:
import pandas as pd
import matplotlib.pyplot as plt
Loading dataset:
data = pd.read_csv("sales_data.csv")

data.head()
Checking missing values:
data.isnull().sum()
Creating revenue column:
data["Revenue"] = data["Quantity"] * data["Price"]
Total revenue:
data["Revenue"].sum()
CHAPTER SEVEN: POWER BI DASHBOARD DESIGN
Dashboard 1: Executive Overview
Contains:
Total Revenue
Total Orders
Total Customers
Average Order Value
Visuals:
KPI Cards
Line Chart
Bar Chart
Dashboard 2: Product Analysis
Shows:
Top 10 products
Product categories
Product contribution to revenue
Dashboard 3: Customer Analysis
Shows:
Highest spending customers
Customer segmentation
Buying frequency
Dashboard 4: Regional Analysis
Shows:
Sales by location
Regional comparison
Growth opportunities
KEY INSIGHTS GENERATED
Example findings:
Electronics generated the highest revenue.
The Northern region recorded the highest number of transactions.
Smartphones were the most purchased product.
Sales increased during festive periods.
A small group of customers contributed significantly to revenue.
BUSINESS RECOMMENDATIONS
Based on the analysis:
Increase stock availability for high-performing products.
Focus marketing campaigns on profitable customer groups.
Improve sales strategies in low-performing regions.
Use customer purchase history for personalized offers.
GITHUB REPOSITORY STRUCTURE
Customer-Sales-Analytics/

├── Dataset
│   └── sales_data.csv

├── SQL
│   └── sales_analysis.sql

├── Python
│   └── sales_analysis.ipynb

├── PowerBI
│   └── sales_dashboard.pbix

├── Images
│   └── dashboard.png

└── README.md
README FILE
# Customer Sales Analytics Project

## Overview
This project analyzes sales transactions using SQL, Python and Power BI.

## Tools Used
- Excel
- SQL
- Python
- Power BI

## Objectives
- Analyze sales trends
- Understand customer behaviour
- Identify revenue drivers

## Results
The project generated insights that support business decision-making.