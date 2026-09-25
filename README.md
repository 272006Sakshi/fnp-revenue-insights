## 🎁 Ferns & Petals (FNP) Sales Analysis (Excel Dashboard)

An end-to-end sales analytics project built entirely in Excel: from raw multi-table data to a fully interactive dashboard for Ferns and Petals (FNP), a gifting company that sells occasion-based products (Anniversary, Birthday, Diwali, Holi, Raksha Bandhan, Valentine's Day).

The project simulates a real analytics workflow: 
**Extract → Transform → Model (Star Schema) → Analyze (DAX/PivotTables) → Visualize (Dashboard).**

---
## 📌 Business Problem

FNP wanted to understand its sales performance and customer behavior to sharpen its sales strategy and improve customer satisfaction. The analysis had to answer:

-  What is the overall revenue?
- What is the average order-to-delivery time?
- How does monthly sales performance fluctuate across 2023?
- Which products are the top revenue generators?
- How much are customers spending on average?
- How do the top 5 products perform in terms of sales?
- Which 10 cities place the highest number of orders?
- Does a higher order quantity impact delivery time?
- How does revenue compare across occasions?
- Which products are most popular for specific occasions?

## 🗂️ Data Collection

The raw data came as three related tables:

**Table	Description**

 **Orders:**	Order ID, order date, delivery date, quantity, occasion, city (fact table)

 **Products:**	Product ID, product name, category, price, Occasion

 **Customers:**	Customer ID, customer details

**Price** was not directly available in the Orders table, so it had to be pulled in from the Products table before revenue could be calculated.

## 🛠️ Tools & Techniques Used

- Excel — end-to-end workbook
- Power Query — data extraction & transformation
- Data Model (Power Pivot) — relational star schema
- DAX — calculated columns
- PivotTables & PivotCharts — analysis
- Slicers — interactive filtering (by Occasion, Order Date, Delivery Date)

## 🔧 Methodology
**Step 1 - Extraction & Transformation (Power Query)**
- Imported the Orders, Products, and Customers tables into Power Query.
- Merged the Products table into Orders to bring in Price (since Orders only had Quantity).
- Added new columns to the Orders table:
  - Order_Time — time component extracted from the order timestamp
  - Diff_Order_Delivery — number of days between order date and delivery date
  - Order_Month — month extracted from the order date
- Loaded the cleaned tables into the Excel Data Model.

**Step 2 - Data Modeling (Star Schema)**

- Built a star schema in the Data Model:
  - Fact table: Orders (transaction-level data)
  - Dimension tables: Products, Customers

This structure keeps the model normalized and makes the PivotTables fast and easy to slice by product or customer attributes.

**Step 3 - DAX Calculated Columns**
- Added two key calculated columns directly in the Data Model:
  - Revenue = Price * Quantity
  - Order_Day_Name = FORMAT(Order_Date, "DDDD")

**Step 4 - Analysis (PivotTables)**

- Used **PivotTables/PivotCharts** built on the Data Model to answer each of the business questions, with Occasion, Order_Date, and Delivery_Date slicers for interactive filtering.

**Step 5 - Dashboard Design**

- Consolidated all the visuals into a single interactive Excel dashboard with **KPI cards, bar charts, a line/trend chart, and slicers.**
