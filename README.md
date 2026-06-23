# 🛍️Retail-Customer-Insights-Dashboard

## 📊 Project Overview

The Retail-Customer-Insights-Dashboard is a comprehensive business intelligence solution designed to analyze customer purchasing patterns, demographic behavior, subscription trends, and revenue performance.

This project transforms raw customer transaction data into actionable insights using Power BI, enabling businesses to make informed decisions and improve customer engagement strategies.

## 🎯 Business Objective

The primary objective of this project is to:

1.Understand customer purchasing behavior

2.Analyze revenue contribution across product categories

3.Identify high-performing customer segments

4.Evaluate subscription impact on sales

5.Monitor customer demographics and ratings

6.Support data-driven business decisions

## DataSet Used
<a href="https://github.com/nikhilsingh7874-alt/Retail-Customer-Insights-Dashboard/blob/main/customer_shopping_behavior.csv">customer_shopping_behavior.csv</a>

## 🛠️ Tools & Technologies Used

| Tool           | Purpose                    |
| -------------- | -------------------------- |
| Power BI       | Dashboard Development      |
| SQL            | Data Extraction & Querying |
| Excel/CSV      | Data Source                |
| DAX            | KPI Calculations           |
| Data Analytics | Insight Generation         |

## 📈 Dashboard Features

![D:\Customer Analysis Project](https://github.com/nikhilsingh7874-alt/Retail-Customer-Insights-Dashboard/blob/main/Dashboard_image.png)


📌 Key Performance Indicators (KPIs)

👥 Total Customers: 3.9K
💰 Average Purchase Amount: $59.76
⭐ Average Customer Rating: 3.75
📌 Interactive Filters

Users can filter data by:

<ul><li>Subscription Status</li><li>Gender</li>
<li>Product Category</li><li>Shipping Type</li></ul>


📌 Visualizations Included

<ul><li>Subscription Status Distribution</li><li>Revenue by Category</li>
<li>Sales by Category</li><li>Revenue by Age Group</li><li>Revenue by Age Group</li><li>Interactive KPI Cards</li> </ul>


## 🔍 Key Insights

💰 Revenue Analysis

<ul><li>Clothing generates the highest revenue (104K).</li><li>Accessories contribute significantly with 74K revenue.</li>
<li>Footwear and Outerwear show opportunities for growth.</li></ul>

👥 Customer Demographics

<ul><li>Young Adults are the highest revenue-generating age group.</li>
<li>Middle-aged customers form a large customer base.</li>
<li>Revenue distribution remains strong across all age groups.</li></ul>

📦 Subscription Behavior

<ul><li>Approximately 73% of customers do not have subscriptions.</li>
<li>Subscription-based customers account for 27% of the customer base.</li>
<li>⭐ Customer Satisfaction</li></ul>

Average customer rating of 3.75/5 indicates generally positive customer experience.

## 📂 Repository Structure

Customer-Behavior-Analytics-Dashboard/
│
├── Dataset/
│   └── customer_shopping_behavior.csv
│
├── SQL Queries/
│   └── customer_behavior_sql_queries.sql
│
├── Power BI Dashboard/
│   └── Customer_Behavior_Dashboard.pbix
│
├── Dashboard Screenshots/
│   └── Dashboard_Image.png
│
├── Documentation/
│   └── Project_Report.pdf
│
└── README.md

## 📌 DAX Measures
-- Total Customers
Total Customers =
DISTINCTCOUNT(Customer[customer_id])

---

-- Total Revenue
Total Revenue =
SUM(Customer[purchase_amount])

---

-- Average Purchase Amount
Average Purchase Amount =
AVERAGE(Customer[purchase_amount])

---

-- Average Review Rating
Average Review Rating =
AVERAGE(Customer[review_rating])

---

-- Total Orders
Total Orders =
COUNT(Customer[customer_id])

---

-- Subscribers Count
Subscribers =
CALCULATE(
COUNT(Customer[customer_id]),
Customer[subscription_status] = "Yes"
)

---

-- Non-Subscribers Count
Non Subscribers =
CALCULATE(
COUNT(Customer[customer_id]),
Customer[subscription_status] = "No"
)

---

-- Subscription %
Subscription % =
DIVIDE(
[Subscribers],
[Total Customers],
0
)

---

-- Revenue by Category
Revenue by Category =
SUM(Customer[purchase_amount])

---

-- Sales Count
Sales Count =
COUNT(Customer[item_purchased])

---

-- Revenue by Age Group
Revenue by Age Group =
SUM(Customer[purchase_amount])

---

-- Female Customers
Female Customers =
CALCULATE(
COUNT(Customer[customer_id]),
Customer[gender] = "Female"
)

---

-- Male Customers
Male Customers =
CALCULATE(
COUNT(Customer[customer_id]),
Customer[gender] = "Male"
)

---

-- Customer Rating Score
Customer Rating Score =
DIVIDE(
SUM(Customer[review_rating]),
COUNT(Customer[review_rating]),
0
)

---

-- Average Previous Purchases
Avg Previous Purchases =
AVERAGE(Customer[previous_purchases])

---

-- Revenue Contribution %
Revenue Contribution % =
DIVIDE(
[Total Revenue],
CALCULATE(
[Total Revenue],
ALL(Customer)
),
0
)

---

-- High Value Customers
High Value Customers =
CALCULATE(
COUNT(Customer[customer_id]),
Customer[purchase_amount] > 100
)

## 👨‍💻 Author

Nikhil Singh

Aspiring Data Analyst | Power BI Developer | SQL Enthusiast

Connect With Me
LinkedIn: https://www.linkedin.com/in/nikhil-singh-48a676327?utm_source=share_via&utm_content=profile&utm_medium=member_android
GitHub: https://github.com/nikhilsingh7874-alt
