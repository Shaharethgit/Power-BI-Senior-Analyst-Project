# Power BI Senior Data Analyst Project

An end-to-end Power BI portfolio project focused on retail sales analytics, data modelling, DAX calculations, and business performance analysis.

---

## 1. Project Overview

This project analyses a multi-year technology retail dataset covering 2022–2025.

The objective is to transform raw business data into meaningful insights that support better decision-making.

## 2. Business Scenario

A retail company wants to understand its business performance across different dimensions.

Key business questions include:

- How are sales performing year over year?
- Which products and categories generate the most revenue?
- How profitable is the business?
- How much revenue is lost through product returns?
- Are stores achieving their monthly sales targets?
- Which customers and employees contribute most to sales?

## 3. Tools & Technologies

| Tool | Purpose |
|---|---|
| Power BI Desktop | Data modelling and visualization |
| Power Query | Data preparation and transformation |
| DAX | Business calculations and analytics |
| Python (Pandas) | Data analysis and transformation |
| Microsoft Excel | Source dataset |

## 4. Dataset

The project uses a synthetic technology retail dataset containing:

- Sales
- Returns
- Products
- Customers
- Stores
- Employees
- Categories
- Monthly Targets

**Coverage:** 2022–2025, with some date records extending into January 2026.

## 5. Project Workflow

### Phase 1 — Data Preparation & Quality Checks
- Data inspection and validation
- Missing value checks
- Duplicate identification
- Data type validation
- Fact-table grain analysis
- Referential integrity checks

### Phase 2 — Data Modelling
- Star schema design
- Fact and dimension table relationships
- Dedicated Date Table
- Active and inactive relationships
- Cross-filter direction configuration

### Phase 3 — DAX Development

**Basic Business Measures**
- Total Sales
- Total Quantity
- Total Orders
- Total COGS
- Gross Profit
- Gross Margin %
- Total Returns
- Net Revenue
- Total Target
- Target Achievement %

**Time Intelligence**
- Previous Year Sales
- Year-over-Year Growth %
- Previous Month Sales
- Month-over-Month Growth %
- YTD Sales
- QTD Sales
- MTD Sales
- Rolling 3, 6 and 12-Month Sales
- Same Period Last Year Sales

### Phase 4 — Business Performance Analysis
- Sales by Category
- Product Performance
- Store Performance
- Customer Analysis
- Employee Performance
- Profitability Analysis
- Target Achievement Analysis

### Phase 5 — Dashboard Development
Interactive dashboards and business insights will be developed using Power BI.

## 6. Repository Structure

```text
Power-BI-Senior-Analyst-Project/
│
├── data/
├── power-bi/
├── dax/
├── power-query/
├── screenshots/
├── documentation/
├── .gitignore
└── README.md
```

## 7. Project Status

- [x] Data preparation and quality checks
- [x] Data modelling
- [x] Basic DAX measures
- [x] Time intelligence measures
- [ ] Business performance analysis
- [ ] Dashboard development
- [ ] Final business insights

## 8. Author

**Power BI Senior Data Analyst Portfolio Project**