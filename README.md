# 🚗 BMW Sales Analysis Using SQL

## 📌 1. Introduction

Data analysis plays an important role in understanding business performance. In the automobile industry, companies analyze sales data to understand demand, customer preferences, and regional market trends.

This project focuses on analyzing BMW car sales data using SQL queries. The dataset contains information about:

* BMW models
* Sales year & month
* Region
* Units sold
* Revenue generated
* Average price
* BEV (Battery Electric Vehicle) share

---

## 🎯 2. Project Objectives

The main objectives of this project are:

* Calculate total BMW car sales and revenue
* Identify top-selling BMW models
* Analyze regional sales performance
* Understand monthly and yearly sales trends
* Evaluate the growth of electric vehicles using BEV share

---

## 🛠️ 3. Tools and Technologies Used

* **SQL** – For querying and analysis
* **MySQL** – Database management system
* **BMW Sales Dataset** – Source of data

---

## 🗄️ 4. Database Creation

```sql
CREATE DATABASE project;
USE project;
```

---

## 📊 5. Dataset Description

The table used in this project is named **BMW** with the following columns:

| Column Name   | Description                  |
| ------------- | ---------------------------- |
| Model         | Name of the BMW car model    |
| Year          | Year of sale                 |
| Month         | Month of sale                |
| Region        | Sales region                 |
| Units_Sold    | Number of cars sold          |
| Revenue_EUR   | Revenue generated (in Euros) |
| Avg_Price_EUR | Average car price            |
| BEV_Share     | Electric vehicle share (%)   |

---

## 💻 6. SQL Queries Used

### 🔹 Basic Queries

```sql
SELECT * FROM BMW;
```

➡️ Displays all records and columns

```sql
SELECT SUM(Units_sold) AS total_sales FROM BMW;
```

➡️ Calculates total units sold

```sql
SELECT SUM(Revenue_EUR) AS total_revenue FROM BMW;
```

➡️ Calculates total revenue

```sql
SELECT * FROM BMW WHERE Year BETWEEN 2019 AND 2020;
```

➡️ Filters data between years

```sql
SELECT DISTINCT(Model) FROM BMW;
```

➡️ Shows unique models

```sql
SELECT AVG(Avg_Price_EUR) FROM BMW;
```

➡️ Finds average price

```sql
SELECT COUNT(Model) FROM BMW;
```

➡️ Counts total records

```sql
SELECT SUM(Avg_Price_EUR) AS total_sales FROM BMW;
```

➡️ Adds all average prices

```sql
SELECT Model FROM BMW WHERE Units_Sold > 500;
```

➡️ Models with high sales

---

### 🔹 Aggregation & Grouping

```sql
SELECT Region, SUM(Units_Sold) AS total_unitsold 
FROM BMW GROUP BY Region;
```

```sql
SELECT Model, SUM(Revenue_EUR) AS total_revenue 
FROM BMW GROUP BY Model;
```

```sql
SELECT Model, SUM(Units_sold) AS total 
FROM BMW GROUP BY Model 
ORDER BY total DESC LIMIT 5;
```

```sql
SELECT Year, AVG(Revenue_EUR) AS average_revenue 
FROM BMW GROUP BY Year;
```

```sql
SELECT MAX(Avg_Price_EUR) AS maximum, 
       MIN(Avg_Price_EUR) AS minimum 
FROM BMW;
```

---

### 🔹 Time-Based Analysis

```sql
SELECT Month, SUM(Units_Sold) AS monthly_sales 
FROM BMW GROUP BY Month;
```

```sql
SELECT Year, AVG(BEV_SHARE) AS average 
FROM BMW GROUP BY Year;
```

```sql
SELECT Month, SUM(Units_Sold) AS monthly_sales 
FROM BMW GROUP BY Month 
ORDER BY Month, monthly_sales DESC;
```

```sql
SELECT Year, AVG(BEV_Share) AS peryear 
FROM BMW GROUP BY Year;
```

---

### 🔹 Advanced Insights

```sql
SELECT Region, SUM(Units_Sold) AS highest_unit 
FROM BMW GROUP BY Region 
ORDER BY highest_unit DESC LIMIT 1;
```

```sql
SELECT Model, Region, SUM(Units_Sold) AS topmodel 
FROM BMW GROUP BY Region, Model 
ORDER BY Region, topmodel DESC;
```

```sql
SELECT Region, SUM(BEV_Share) AS highest 
FROM BMW GROUP BY Region 
ORDER BY highest DESC;
```

```sql
SELECT Region, SUM(Units_Sold) AS top 
FROM BMW GROUP BY Region 
ORDER BY top DESC;
```

```sql
SELECT Year, SUM(Revenue_EUR) AS highest 
FROM BMW GROUP BY Year 
ORDER BY highest DESC;
```

---

## 🔍 7. Key Findings

* Certain BMW models consistently outperform others in sales
* Regional analysis highlights top-performing markets
* Monthly trends reveal peak sales periods
* Yearly revenue shows overall business growth patterns
* BEV share indicates rising importance of electric vehicles

---

## ✅ 8. Conclusion

This project demonstrates how SQL can be used to analyze real-world business data effectively.

Using SQL functions like:

* `SUM()`
* `AVG()`
* `COUNT()`
* `GROUP BY`
* `ORDER BY`

we extracted meaningful insights from BMW sales data.

📈 These insights help businesses make **data-driven decisions** and improve strategic planning.

---

## ⭐ Bonus (Optional for GitHub)

You can add this at the end:

```md
## 📎 Author
Aryakrishna U

## 🔗 Project Type
SQL Data Analysis Project (Beginner → Intermediate)

## 💡 Future Improvements
- Add Power BI Dashboard
- Add Python (Pandas + Matplotlib) analysis
- Include real-time dataset
```

---

If you want, I can next:
✅ Add **GitHub badges & design (very professional)**
✅ Convert this into **LinkedIn post**
✅ Add **Power BI dashboard section**

Just tell 👍
