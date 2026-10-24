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
```

## Key Business Insights
### 1. Customer Segments
* Consumer: 50.56% of total revenue ($1,161,401)

* Corporate: 30.74% of total revenue ($706,146)

* Home Office: 18.70% of total revenue ($429,653)

## 2. Product Category & Profitability
* Technology: Drives the largest revenue share (36.4%) with 1,544 orders. High-margin enterprise copiers (such as the Canon imageCLASS 2200) are the top profit generators.

* Furniture: Accounts for 32.3% of revenue (1,764 orders).

* Office Supplies: Generates 31.3% of revenue with the highest volume (3,742 orders).

## 3. Regional & State Performance
### Top Revenue States:

* California (West): $457,687

* New York (East): $310,876

* Texas (Central): $170,188

* Washington (West): $138,641

* Pennsylvania (East): $116,511

### Bottom Revenue States: 
* North Dakota ($919), West Virginia ($1,209), Maine ($1,270), South Dakota ($1,315), Wyoming ($1,600).

### Most Profitable Region: 
* West Region (~$108K–$140K total profit).

## 4. Seasonality & Trends
* February Dip: Consistently the lowest revenue month across historical years (2014, 2015, 2017).

* October Anomalies: Sharp drops in sales activity occur every October before rebounding.

* Q4 Peak: Strong sales surge in November and December driven by year-end commercial demand.

## 🎯 Strategic Recommendations
* Focus on High-Margin Copiers: Prioritize stocking and marketing top-tier office copiers, as they account for the majority of individual product profits.

* Optimize Low-Performing Regions: Re-evaluate distribution strategies and marketing spend in low-revenue states like North Dakota and West Virginia.

* Smooth Out Seasonality: Introduce targeted promotions during February and October to steady cash flow throughout the year.

## How to Use This Repository
### Clone the repository:

Bash
```git clone [https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git)```
* Open the .pbix file in Power BI Desktop to explore interactive charts, cross-filtering, and DAX measures.
