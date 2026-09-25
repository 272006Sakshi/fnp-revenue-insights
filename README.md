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
