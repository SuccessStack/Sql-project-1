# 📊 Walmart Sales Data Analysis using MYSQL

## 📝 About the Project

This project explores the Walmart Sales dataset to gain insights into:

- Top-performing branches and product lines
- Sales trends across different dimensions
- Customer behavior and segmentation
- Optimization opportunities for sales strategies

The dataset was obtained from the **Kaggle Walmart Sales Forecasting Competition**, which involves historical sales data for Walmart branches and departments. The challenge includes forecasting future sales and understanding the effects of events like holiday markdowns.

## 🎯 Project Objectives

- Identify key drivers of revenue across branches and product lines.
- Understand sales trends and customer purchasing behavior.
- Evaluate customer types and their contribution to sales and profit.
- Generate actionable insights to optimize business decisions.

---

## 📦 About the Data

The dataset consists of **1000 records** with **17 columns**. It captures transactional sales data from Walmart branches in **Mandalay**, **Yangon**, and **Naypyitaw**.

### 📌 Column Descriptions

| Column                   | Description                                     | Data Type         |
|--------------------------|-------------------------------------------------|--------------------|
| `invoice_id`             | Unique identifier for the transaction           | VARCHAR(30)        |
| `branch`                 | Branch code (A, B, C)                           | VARCHAR(5)         |
| `city`                   | Location of the branch                          | VARCHAR(30)        |
| `customer_type`          | Type of customer (Member/Normal)                | VARCHAR(30)        |
| `gender`                 | Gender of the customer                          | VARCHAR(10)        |
| `product_line`           | Category of the product sold                    | VARCHAR(100)       |
| `unit_price`             | Price per unit                                  | DECIMAL(10,2)      |
| `quantity`               | Number of items sold                            | INT                |
| `VAT`                    | Value-added tax (5% of COGS)                    | FLOAT(6,4)         |
| `total`                  | Total cost (COGS + VAT)                         | DECIMAL(10,2)      |
| `date`                   | Date of transaction                             | DATE               |
| `time`                   | Time of transaction                             | TIMESTAMP          |
| `payment_method`         | Payment type used                               | VARCHAR            |
| `cogs`                   | Cost of Goods Sold                              | DECIMAL(10,2)      |
| `gross_margin_percentage`| Margin % of the transaction                     | FLOAT(11,9)        |
| `gross_income`           | Gross income from transaction                   | DECIMAL(10,2)      |
| `rating`                 | Customer rating (1–10)                          | FLOAT(2,1)         |

---

## 🧰 Approach Used

### 1. Data Wrangling
- Inspected the data for null/missing values.
- No null values detected (all fields set to `NOT NULL` at database creation).

### 2. Feature Engineering
- `time_of_day`: Morning, Afternoon, Evening (from transaction time)
- `day_name`: Day of the week (Mon–Sun)
- `month_name`: Month name (Jan–Dec)

### 3. Database Creation
- Tables created and populated using SQL.
- Views and queries structured for performance analysis.

### 4. Exploratory Data Analysis (EDA)
- Analysis conducted to answer specific business questions on product sales, customer segments, and sales trends.

---

## 📌 Business Questions

### 🔹 Generic
- How many unique cities exist in the dataset?
- Which branch is in which city?

### 🔹 Product Analysis
- How many unique product lines are there?
- What is the most common payment method?
- What is the most sold product line?
- What is the total revenue by month?
- Which month had the highest COGS?
- Which product line had the largest revenue?
- Which city generated the most revenue?
- Which product line had the highest VAT?
- Classify product lines as “Good” or “Bad” based on average sales.
- Which branch sold more products than the average?
- What is the most common product line by gender?
- What is the average rating per product line?

### 🔹 Sales Analysis
- Number of sales by time of day per weekday.
- Which customer type brings the most revenue?
- Which city has the highest average VAT?
- Which customer type pays the most in VAT?

### 🔹 Customer Analysis
- How many unique customer types are there?
- How many unique payment methods exist?
- What is the most common customer type?
- Which customer type buys the most?
- What is the gender distribution overall and per branch?
- Which time of day do customers give the most ratings (overall and per branch)?
- Which day of the week has the highest average rating (overall and per branch)?

---

## 💡 Advanced Analysis (Complex Questions)

- Analyze sales trend over time by **month and year**.
- Determine average spending by **customer type and gender**.
- Evaluate **product line performance per branch**.
- Analyze **revenue contribution by time of day and day of the week**.
- Find correlation between **quantity sold and customer rating**.
- Identify customers who spent **above a certain threshold**.
- Determine sales by **season (spring, summer, autumn, winter)**.
- Identify top 5 cities with the **highest sales per product line**.
- Measure **branch efficiency by revenue per product line**.
- Identify **repeat customers** and analyze spending behavior.

---

## 🧮 Revenue and Profit Calculations

### Formulas:

- **COGS** = `unit_price × quantity`
- **VAT** = `0.05 × COGS`
- **Total (gross sales)** = `COGS + VAT`
- **Gross Income** = `Total - COGS`
- **Gross Margin** = `Gross Income / Total`

---

