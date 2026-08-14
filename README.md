# Amazon Seller SQL Data Analytics Project

##  Project Overview

This project analyzes an **Amazon Seller e-commerce dataset containing 1,000 orders** using **SQL (SQLite)** to identify sales trends, customer behavior, product performance, payment preferences, and operational insights.

The project demonstrates an end-to-end **Data Analyst workflow** — from querying raw transactional data to generating meaningful business recommendations.

---

## Business Objectives

* Identify top-performing product categories and products
* Analyze revenue and order performance
* Understand customer behavior across cities
* Analyze payment-method preferences
* Identify high-value and high-discount orders
* Analyze orders with higher quantities
* Evaluate order-status performance
* Identify opportunities to improve sales and operations

---

## Dataset

The dataset contains **1,000 e-commerce transactions** with fields including:

| Column             | Description         |
| ------------------ | ------------------- |
| `order_id`         | Unique order ID     |
| `order_time`       | Order date and time |
| `product_name`     | Product purchased   |
| `category`         | Product category    |
| `seller_id`        | Seller identifier   |
| `seller_state`     | Seller state        |
| `customer_area`    | Customer area       |
| `customer_city`    | Customer city       |
| `quantity`         | Quantity purchased  |
| `unit_price`       | Product unit price  |
| `discount_percent` | Discount percentage |
| `order_value`      | Final order value   |
| `payment_method`   | Payment method      |
| `order_status`     | Order status        |
| `delivery_date`    | Delivery date       |

---

##  Tools & Technologies

* **SQL**
* **SQLite**
* **CSV**
* **Data Analysis**
* **Business Intelligence**
* **GitHub**

### SQL Concepts Used

```text
SELECT
WHERE
ORDER BY
LIMIT
COUNT()
SUM()
AVG()
GROUP BY
HAVING
CASE WHEN
Subqueries
Aggregate Functions
Filtering
Sorting
Ranking
```

---

## Key SQL Analysis

### 1. Top Discounted Products

```sql
SELECT discount_percent,
       category,
       order_value,
       product_name
FROM amazon_seller
ORDER BY discount_percent DESC
LIMIT 10;
```

### 2. Highest-Value Orders

```sql
SELECT order_value,
       product_name,
       category
FROM amazon_seller
ORDER BY order_value DESC
LIMIT 5;
```

### 3. Orders With Quantity Greater Than 2

```sql
SELECT quantity,
       customer_city,
       product_name
FROM amazon_seller
WHERE quantity > 2
ORDER BY quantity DESC
LIMIT 10;
```

### 4. Recent Mumbai Orders

```sql
SELECT *
FROM amazon_seller
WHERE customer_city = 'Mumbai'
ORDER BY order_time DESC
LIMIT 5;
```

### 5. Payment Method Analysis

```sql
SELECT payment_method,
       COUNT(*) AS payment_count
FROM amazon_seller
GROUP BY payment_method
ORDER BY payment_count DESC;
```

---

## Key Business Insights

### Electronics Performance

Electronics is the strongest revenue-generating category in the dataset. This indicates an opportunity to:

* Maintain higher product availability
* Monitor inventory levels
* Promote high-performing electronics
* Analyze product-level demand

### Customer Geography

Cities such as **Mumbai, Pune, Kolkata, Hyderabad and Delhi** provide valuable opportunities for customer and revenue analysis.

Businesses can use city-level performance to optimize:

* Inventory
* Marketing campaigns
* Delivery capacity
* Regional promotions

### Payment Behavior

**UPI** is the most frequently used payment method in the dataset.

This suggests that maintaining a fast and convenient UPI checkout experience can support customer conversion.

### Order Quantity

Orders with quantity greater than 2 can be analyzed to identify:

* Bulk-buying behavior
* Popular products
* Potential bundle opportunities
* Customer segments with higher purchase volume

### Order Operations

Returned and cancelled orders should be investigated by:

* Product
* Category
* Seller
* Customer city
* Payment method

This can help identify operational problems and improve customer experience.

---

## Business Recommendations

1. **Prioritize Electronics**
   Focus inventory and marketing efforts on high-performing electronics products.

2. **Optimize Regional Strategy**
   Use city-level revenue data to target high-value customer markets.

3. **Improve Payment Experience**
   Keep UPI highly visible while supporting other payment options.

4. **Reduce Returns & Cancellations**
   Analyze product-level and seller-level return patterns to identify root causes.

5. **Improve Product Performance**
   Compare product revenue, quantity, discount and order frequency before making pricing or inventory decisions.

---

## Project Structure

```text
amazon-seller-sql-analysis/
│
├── data/
│   └── amazon_seller.csv
│
├── sql/
│   └── amazon_seller_analysis.sql
│
├── screenshots/
│   └── query_results/
│
├── documentation/
│   └── Amazon_Seller_SQL_Data_Analytics_Project.pdf
│
└── README.md
```

---

## Skills Demonstrated

* SQL Data Analysis
* Data Cleaning & Validation
* Exploratory Data Analysis
* KPI Analysis
* Sales Analysis
* Customer Analysis
* Product Analysis
* Payment Analysis
* Business Insights
* Data Storytelling

---

## Portfolio Project

**Project:** Amazon Seller SQL Data Analytics
**Role:** Data Analyst
**Dataset:** 1,000 E-commerce Orders
**Database:** SQLite
**Primary Skill:** SQL

### Resume Description

> Analyzed 1,000 e-commerce transactions using SQL to identify category, product, city, payment and order-status trends. Generated actionable business insights around revenue performance, customer geography, payment behavior and operational efficiency.

---

## Conclusion

This project demonstrates how SQL can be used to transform raw e-commerce transaction data into **actionable business insights**.

The analysis follows a practical Data Analyst workflow:

**Raw Data → SQL Queries → Analysis → Insights → Business Recommendations**
