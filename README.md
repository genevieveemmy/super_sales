# 📊 Super Store Sales Performance Dashboard

An end-to-end **Power BI** business intelligence solution designed to analyze sales performance, regional profitability, customer segmentation, and product trends across a multi-region retail operation ($2.30M Total Revenue).

---

## 📌 Executive Summary

This interactive dashboard translates raw transaction data into actionable business insights using pure **Power BI**—utilizing **Power Query** for data transformation, a robust data model, and custom **DAX measures** for dynamic analysis.

### Key Metrics
* **Total Revenue:** $2.30M
* **Total Profit:** $286K
* **Profit Margin:** 12.0%
* **Total Orders:** 5,000 orders (5,009 total category line items)
* **Average Order Value (AOV):** $230

---

## 🛠️ Power BI Implementation & Workflow

### 1. Data Cleaning & Transformation (Power Query)
* **Data Cleansing:** Stripped whitespace, handled missing values, and validated column types across all source fields.
* **Date Data Type Standardization:** Transformed order and shipment date columns from text format to Date data types in Power Query to enable time-intelligence function modeling and chronological DAX calculations
* **Custom Columns:** Added custom conditional columns in Power Query M code to standardize regional and state tags.


---

## 🧮 DAX Measures Included

Key calculations built using Data Analysis Expressions (DAX):

```dax
// Total Revenue
Total Revenue = SUM(Sales[Sales Amount])

// Total Profit
Total Profit = SUM(Sales[Profit])

// Profit Margin %
Profit Margin = DIVIDE([Total Profit], [Total Revenue], 0)

// Total Orders Count
Total Orders = DISTINCTCOUNT(Sales[Order ID])

// Average Order Value (AOV)
Average Sales = DIVIDE([Total Revenue], [Total Orders], 0)

// Category Order Count
Category Count of Order ID = COUNT(Sales[Order ID])
