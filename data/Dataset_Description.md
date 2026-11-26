# Dataset Description

## 1. Dataset Overview

This project uses a synthetic technology retail dataset covering 2022–2025, with some records extending into January 2026.

The dataset is designed to simulate a real-world retail business and support business intelligence and data analytics.

## 2. Tables Overview

| Table | Type | Description |
|---|---|---|
| Sales | Fact | Sales transactions and revenue details |
| Returns | Fact | Product return transactions |
| Products | Dimension | Product details and categories |
| Customers | Dimension | Customer information |
| Stores | Dimension | Store details |
| Employees | Dimension | Employee information |
| Categories | Dimension | Product category information |
| MonthlyTargets | Fact | Monthly sales targets by store and category |

## 3. Data Grain

| Table | Grain |
|---|---|
| Sales | One row per order |
| Returns | One row per return transaction |
| MonthlyTargets | One row per month, store, and category |
| Products | One row per product |
| Customers | One row per customer |
| Stores | One row per store |
| Employees | One row per employee |
| Categories | One row per category |

## 4. Data Model

The model uses a star-schema approach with dimension tables filtering fact tables.

### Main Relationships

- Products → Sales
- Customers → Sales
- Stores → Sales
- Employees → Sales
- Categories → Products
- Categories → MonthlyTargets
- DateTable → Sales
- DateTable → Returns
- DateTable → MonthlyTargets

Additional relationships connect product, customer, store, and employee dimensions to the Returns table.

### Date Relationships

- DateTable[Date] → Sales[OrderDate] — Active
- DateTable[Date] → Sales[ShipDate] — Inactive
- DateTable[Date] → Returns[ReturnDate] — Active
- DateTable[Date] → MonthlyTargets[MonthStart] — Active

## 5. Data Quality Checks

- Primary key uniqueness
- Duplicate record identification
- Missing value checks
- Data type validation
- Foreign key validation
- Fact-table grain verification
- Monthly target uniqueness

## 6. Business Analysis Opportunities

- Sales and revenue trends
- Product and category performance
- Gross profit and gross margin
- Customer purchasing behaviour
- Store performance
- Employee performance
- Product returns
- Monthly target achievement
- Year-over-year sales growth