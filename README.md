# 🛒 Retail Sales Analysis Project

This project aims to analyze retail sales data using SQL and visualize sales patterns, category trends, and regional performance. The insights are useful for understanding customer demand, sales performance, and product optimization.

---

## 📌 Overview

- ✅ **Dataset Used:** Retail sales records (products, categories, regions, sales, quantities)
- ✅ **Data Format:** CSV & SQL
- ✅ **Tools Used:** SQL
- ✅ **Objective:** Identify top-selling products, regions, sales performance, and stock issues

---

## 📊 Key Analysis Areas

- 🛍️ Top-selling products by revenue and quantity
- 📦 Inventory stock levels vs sales
- 🌍 Regional and category-wise sales performance
- 📈 Monthly/quarterly trends in revenue and units sold
- ❗ Identifying underperforming products or regions

---

## 🧠 Sample Questions Solved

- What are the top 10 products by revenue?
- Which region generated the highest sales?
- Are any product categories declining in performance?
- What is the total monthly revenue across all branches?
- How do quantity sold and revenue correlate over time?

---

## 📄 SQL Snippets Example

```sql
-- Total revenue by product
SELECT ProductName, SUM(Revenue) AS TotalRevenue
FROM retail_sales
GROUP BY ProductName
ORDER BY TotalRevenue DESC
LIMIT 10;

-- Region-wise monthly sales trend
SELECT Region, MONTH(SaleDate) AS Month, SUM(Revenue) AS MonthlyRevenue
FROM retail_sales
GROUP BY Region, MONTH(SaleDate)
ORDER BY Region, Month;


