# 🛍️ Retail Sales Analysis – SQL Project

## 📌 Project Overview
This beginner-friendly SQL project teaches you how to explore and analyze retail sales data. You’ll build a small database, clean it up, and answer real business questions with SQL.

---

## 🎯 Objectives
1. Create and set up a retail sales database.  
2. Clean the data (remove rows with missing values).  
3. Explore the data (EDA).  
4. Write SQL queries to answer business questions.

---

## 🗂️ Database Setup
**Database:** `sql_project1`  
**Main Table:** `retail_sales`

```sql
CREATE TABLE retail_sales (
    transactions_id INT PRIMARY KEY,
    sale_date DATE,
    sale_time TIME,
    customer_id INT,
    gender VARCHAR(10),
    age INT,
    category VARCHAR(35),
    quantity INT,
    price_per_unit FLOAT,
    cogs FLOAT,
    total_sale FLOAT
);
```

---

## 🧹 Data Cleaning
```sql
-- Record, customer, and category counts
SELECT COUNT(*) FROM retail_sales;
SELECT COUNT(DISTINCT customer_id) FROM retail_sales;
SELECT DISTINCT category FROM retail_sales;

-- Delete rows with NULLs
DELETE FROM retail_sales
WHERE sale_date IS NULL OR sale_time IS NULL OR customer_id IS NULL 
  OR gender IS NULL OR age IS NULL OR category IS NULL 
  OR quantity IS NULL OR price_per_unit IS NULL OR cogs IS NULL;
```

---

##📊 Business Questions (with SQL)
1.Sales on a specific date
2.Clothing sales in Nov 2022 with quantity ≥ 4
3.Total sales per category
4.Average age of Beauty category customers
5.Transactions with total sale > 1000
6.Transactions by gender per category
7.Best-selling month each year
8.Top 5 customers by total sales
9.Unique customers per category
10.Sales shift analysis (Morning, Afternoon, Evening)


---

## 🧠 Key Insights
- Clothing & Beauty are strong categories.  
- Some customers make high‑value purchases.  
- Sales vary by month and time of day.  
- Top 5 customers contribute a big share of revenue.

---

## 🚀 How to Run
1. Import the database and table into pgAdmin or any SQL tool.
2.Copy and run the SQL queries.
3.Modify queries to explore more!



## 🏁 Conclusion
This project is a great start for learning SQL. It covers real-life retail data analysis, helping you practice cleaning, exploring, and answering business questions with SQL.
