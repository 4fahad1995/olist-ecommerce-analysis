# Olist E-Commerce Data Analysis

## Data Analysis and Visualization using Power BI

An end-to-end data analytics project analyzing the Olist Brazilian e-commerce marketplace. The project focuses on sales performance, customer behavior, product categories, and delivery operations.

Data was cleaned and validated using Excel, analyzed using PostgreSQL/SQL and Python, and transformed into interactive Power BI dashboards to identify business trends, performance gaps, and actionable insights.

---

## Business Problem

Olist operates a large e-commerce marketplace connecting customers and sellers across Brazil. With a large volume of orders, products, customers, and delivery records, analyzing this data can help identify patterns in sales performance, customer behavior, product demand, and delivery operations.

The objective of this project was to analyze Olist's historical e-commerce data and turn the findings into meaningful business insights and recommendations.

---

## Project Objectives

The analysis focused on four key areas:

### Sales & Revenue Performance
- Analyze total sales, order volume, average order value, and sales by category and customer state.
- Identify the strongest-performing product categories and regions.

### Customer Behavior
- Understand customer acquisition and repeat purchasing behavior.
- Analyze unique customers, repeat customers, and average orders per customer.
- Identify differences in customer behavior across Brazilian states.

### Delivery Operations
- Measure delivery performance and identify late deliveries.
- Analyze average delivery time and late-delivery rates across product categories and over time.
- Identify areas where delivery performance could be improved.

### Business Recommendations
- Identify opportunities to improve customer retention, sales performance, and delivery operations.
- Translate the findings into practical business recommendations.

---

## Data Sources

The analysis used the Olist Brazilian E-Commerce Dataset.

Main datasets:

- **Orders Dataset** — order IDs, customer IDs, order status, purchase dates, approval dates, delivery dates, and estimated delivery dates.
- **Order Items Dataset** — products purchased within each order, sellers, product prices, and freight values.
- **Products Dataset** — product IDs and product category information.
- **Customers Dataset** — customer IDs, unique customer IDs, and customer states.
- **Product Category Translation Dataset** — used to translate Portuguese product category names into English.

---

## Tools Used

| Tool | Purpose |
|---|---|
| Excel | Data cleaning, category translation, duplicate checks, and data-quality validation |
| PostgreSQL / SQL | Data extraction, analysis, aggregations, and business-focused queries |
| Python / Pandas | Additional data analysis and customer/cohort analysis |
| Power BI | Interactive dashboards, KPIs, visualizations, filtering, and business insights |

---

## Analysis Approach

The project followed an end-to-end analytics workflow:

**Raw Data → Cleaning & QA → SQL Analysis → Python Analysis → Power BI → Business Insights & Recommendations**

This approach allowed the data to be validated before analysis and then transformed into interactive dashboards for business decision-making.

---

## Data Cleaning & Preparation

Key data preparation steps included:

- Cleaning and parsing timestamp fields.
- Handling missing values without removing records without sufficient evidence.
- Creating a `purchase_month` field for monthly analysis.
- Calculating `delivery_time` and `delivery_days`.
- Creating a `delivery_status` classification:
  - On Time/Early
  - Late
  - Cannot Check
- Performing date-quality validation checks.
- Translating product categories into English.
- Joining product, order item, and category information.
- Checking duplicates and data quality before analysis.

The final cleaned orders dataset contained **99,441 orders**.

---

## Power BI Dashboards

The final Power BI report contains multiple dashboard sections covering the main areas of analysis.

### Delivery & Operations

Focuses on:

- Average delivery days
- On-time/early delivery rate
- Late deliveries
- Late-delivery rate
- Late-delivery performance by product category
- Average delivery time by category
- Delivery performance over time

### Customer Insights

Focuses on:

- Total customers
- Repeat customers
- Average orders per customer
- New vs repeat customer behavior
- Average order value over time
- Orders by customer state

### Sales & Revenue Performance

Focuses on:

- Total sales
- Total orders
- Total items sold
- Average order value
- Sales by customer state
- Sales by product category
- Sales by order status

---

## Key Findings

### Delivery Performance

- **89.15%** of orders were delivered on time or early.
- **7.87%** of orders were delivered late.
- **2.98%** could not be evaluated because of incomplete delivery information.
- The evaluable-order late-delivery rate was **8.11%**.
- March 2018 had the highest late-delivery rate at **21.36% across 7,003 checkable orders**.
- October 2016 had the lowest late-delivery rate at **1.11% across 270 checkable orders**.

### Customer Behavior

- The business had **96,096 unique customers** across 99,441 orders.
- Only **2,997 customers** placed more than one order.
- The average number of orders per customer was **1.03**.
- New customers grew substantially, reaching **7,430 in November 2017**, compared with **765 in January 2017**.

### Sales Performance

- Total sales reached approximately **13.59M** across 99,441 orders.
- Average order value was approximately **136.68**.
- **São Paulo** generated approximately **5.13M** in sales, making it the strongest-performing customer state.
- **Health & Beauty** was the top sales category at approximately **1.26M**.
- **Watches & Gifts** generated approximately **1.21M** in sales.
- Delivered orders accounted for approximately **97.3% of total sales value**.

---

## Business Recommendations

Based on the analysis, five main recommendations were identified:

1. **Improve customer retention**  
   Introduce personalized offers, post-purchase communication, and incentives for a second purchase to encourage repeat ordering.

2. **Improve delivery performance**  
   Investigate the causes of late deliveries and prioritize periods, categories, and operational areas with consistently higher delay rates.

3. **Prepare for high-demand periods**  
   Use historical demand patterns to plan inventory, fulfillment capacity, and delivery resources ahead of high-demand periods.

4. **Focus on high-revenue categories**  
   Prioritize high-revenue categories for inventory availability and targeted promotions while monitoring their delivery performance.

5. **Strengthen major markets**  
   Prioritize logistics, inventory availability, and customer initiatives in major markets such as São Paulo while using their performance as a benchmark for other regions.

---

## Project Structure

```text
olist-ecommerce-analysis/
│
├── Olist_Dashboard.pbix
│
├── Screenshots/
│   ├── delivery-operations.png
│   ├── customer-insights.png
│   └── sales-revenue.png
│
├── Olist E-Commerce Documentation.docx
│
└── README.md
