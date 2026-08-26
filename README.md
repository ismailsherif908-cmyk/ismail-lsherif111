

# Superstore Sales & Profitability Dashboard

## Project Overview

This project analyzes the **Sample Superstore** retail/e-commerce dataset to understand sales performance, profitability, customers, regions, products, discounts, and shipping performance.

The project includes data cleaning, business questions, analysis, and a Power BI dashboard designed to turn the dataset into clear business insights.

## Dataset

- **Source:** Sample Superstore public retail/e-commerce dataset
- **Raw file:** `data/superstore_raw.csv`
- **Time range:** 2015–2018
- **Raw rows:** 10,800
- **Clean rows:** 9,994
- **Columns:** 21 original columns → 25 after calculated columns
- **Data grain:** One row represents one line item within an order.

### Key Fields

- Order ID, Order Date, Ship Date
- Customer ID, Customer Name, Segment
- Country, City, State, Postal Code, Region
- Product ID, Category, Sub-Category, Product Name
- Sales, Quantity, Discount, Profit

## Data Cleaning

The data was cleaned using **Python/pandas** and the same steps were mirrored in **Power Query M** for Power BI.

Main cleaning operations:

1. Removed 806 rows with missing Order Date.
2. Checked and removed exact duplicate rows.
3. Fixed data types for dates, integers, and decimal values.
4. Converted Postal Code to 5-digit text.
5. Trimmed unnecessary whitespace.
6. Standardized text casing for categories, segments, regions, and ship modes.
7. Checked for duplicate Row IDs.
8. Added calculated columns:
   - Order Year
   - Order Month
   - Shipping Days
   - Profit Margin

The final cleaned dataset contains **9,994 rows and 25 columns**.

## Business Questions & Key Insights

### 1. What are the overall sales, profit, and order volume?

- Sales: **$2.30M**
- Profit: **$286K**
- Profit Margin: **12.5%**
- Distinct Orders: **5,009**

This provides the overall baseline for the business.

### 2. Which category makes the most sales vs. the most profit?

**Technology** leads in profit with approximately **$145K**, while Furniture has similar sales but significantly lower profitability.

### 3. Which sub-categories are losing money?

- **Tables:** approximately **-$17.7K**
- **Bookcases:** approximately **-$3.5K**

Copiers, Phones, and Accessories are among the strongest profit drivers.

### 4. How do sales and profit break down by region?

The **West** region generates about **32% of sales**, followed by the East. The South is the smallest region but remains profitable per dollar of sales.

### 5. What does the sales trend look like over time?

Sales show clear seasonality:

- Sales increase during **November and December**.
- Sales typically dip during **February**.

This can support inventory and campaign planning.

### 6. Who are the top customers by revenue?

The top 10 customers generate approximately **$12K–$25K each in sales**, making them important customers for account management and retention.

### 7. Does discounting help or hurt profit?

Discounting has a negative relationship with profit, with a correlation of approximately **-0.22**.

At discounts above roughly **30%**, average profit becomes negative. This is an important pricing-policy warning.

### 8. How fast do orders ship by ship mode?

| Ship Mode | Approx. Shipping Time |
|---|---:|
| Same Day | 0 days |
| First Class | 2.2 days |
| Second Class | 3.2 days |
| Standard Class | 5 days |

These results also help validate the shipping data.

### 9. Which customer segment drives the business?

The **Consumer** segment is the largest:

- Sales: approximately **$1.16M**
- Profit: approximately **$134K**

It performs ahead of Corporate and Home Office.

## Dashboard

The Power BI dashboard includes:

- Total Sales KPI
- Total Profit KPI
- Total Orders KPI
- Average Discount KPI
- Monthly Sales Trend
- Sales vs. Profit by Category
- Sales by Region
- Profit by Sub-Category
- Average Profit by Discount %

The dashboard is designed to provide a complete business story across **sales, profitability, products, regions, customers, time, and discounts**.

## Main Business Recommendations

1. Review the pricing strategy for discounts above approximately **30%**.
2. Investigate **Tables and Bookcases** because they generate negative profit.
3. Focus on **Technology**, Copiers, Phones, and Accessories as strong profit drivers.
4. Use the November/December sales increase for inventory and marketing planning.
5. Give additional attention to high-revenue customers.
6. Use regional performance to guide marketing and expansion decisions.

## Project Structure

```text
Superstore-Project/
│
├── data/
│   ├── superstore_raw.csv
│   └── superstore_clean.csv
│
├── scripts/
│   ├── clean_data.py
│   └── business_questions_output.txt
│
├── powerquery/
│   └── PowerQuery_M_Steps.pq
│
├── data/
│   └── cleaning_log.txt
│
├── dashboard/
│   └── Superstore_Dashboard.pbix
│
└── README.md
```

## Tools Used

- **Python / pandas** — Data cleaning and preparation
- **Power Query** — Data transformation in Power BI
- **Power BI** — Data visualization and dashboard
- **GitHub** — Project documentation and version control

## Project Goal

The goal of this project is to transform raw Superstore data into a reliable, business-focused dashboard that helps identify:

- What is selling
- What is profitable
- Which products are losing money
- Which regions and customer segments perform best
- How discounts affect profitability
- How sales change over time
- Which customers deserve more attention

---

**Project:** Superstore Sales & Profitability Dashboard  
**Author:** Ismail Sherif Ismail
