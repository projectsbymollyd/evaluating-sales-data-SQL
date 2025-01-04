# Corporation Sales Data Analysis with SQL

For this project, I used SQL to clean and analyze data from a multinational retail corporation in order to help them uncover insights and solve business problems. 🚀 

## 📋 Project Overview

This project focuses on:
1. Identifying the **top-performing products** in each category based on total sales and profit.
2. Using SQL to handle **missing data** by estimating missing quantities in orders using calculated unit prices.

SQL techniques used in this project include ranking, window functions, data aggregation, and handling missing values.

---

## 📊 Key SQL Queries

### 1️⃣ Task 1 🏆
First, I  wanted to identify the top 5 products in each category based on total sales, ranked in descending order of sales within each category. 

**Solution Highlights:**  
- Used SQL **window functions** (`RANK()` with `PARTITION BY`) to rank products by sales within each category.  
- Calculated total sales and profits with **aggregation** (`SUM()`).  
- Rounded values to 2 decimal places for better readability.

**Output Columns:**  
- `category`  
- `product_name`  
- `product_total_sales` (rounded to two decimal places)  
- `product_total_profit` (rounded to two decimal places)  
- `product_rank`

- 

### 2️⃣ Task 2 🛠️  
Then, I estimated the missing values in the `quantity` column by calculating the unit price for products and using it to determine the missing quantities.

**Solution Highlights:**  
- Used a **common table expression (CTE)** to isolate rows with missing quantities.  
- Calculated unit prices based on existing data with `sales / quantity`.  
- Estimated missing quantities by dividing `sales` by the calculated `unit_price`.  
- Rounded results to zero decimal places for clarity.

**Output Columns:**  
- `product_id`  
- `discount`  
- `market`  
- `region`  
- `sales`  
- `quantity`  
- `calculated_quantity` (rounded to zero decimal places)

---

## 📂 About the Dataset  

The dataset includes information about:  
- **Products**: Categories, names, and IDs.  
- **Orders**: Sales, profit, quantity, discount, and region details.  

---

## 💡 What I Learned  

- Leveraging SQL window functions for advanced analytics.  
- Creative approaches to handle missing data.  
- Writing modular, reusable SQL code using CTEs.  

---
