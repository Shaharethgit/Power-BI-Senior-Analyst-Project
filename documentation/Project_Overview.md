# Project Overview

## Project Title
Power BI Senior Data Analyst — Retail Business Analysis

## Business Objective

The objective of this project is to analyse a multi-year retail dataset and develop business insights using Power BI.

The project focuses on understanding sales performance, profitability, customer behaviour, product returns, and target achievement.

## Business Questions

1. How are sales performing across different years?
2. Which product categories generate the highest revenue?
3. Which products contribute the most profit?
4. How does gross margin vary across categories?
5. Which stores achieve their sales targets?
6. What is the trend in product returns?
7. How do customers contribute to overall revenue?
8. Which employees generate the highest sales?

## Technical Approach

### Data Preparation
Power Query and Python (Pandas) are used for data inspection, transformation, and validation.

### Data Modelling
A relational data model connects sales and returns with relevant dimension tables.

### DAX Development
DAX measures are used for business calculations, time intelligence, and performance analysis.

### Business Analysis
Power BI visuals will be used to explore business performance and communicate insights.

## Expected Deliverables

- Prepared and validated dataset
- Power BI data model
- Documented DAX measures
- Business performance analysis
- Interactive Power BI dashboard
- Business insights and recommendations

## Project Scope

This project demonstrates practical data analyst skills through an end-to-end business intelligence workflow.

## Business Performance Analysis

### Task 1 — Sales by Category

**Objective:** Analyse total sales across different product categories.

**Power BI Visual:** Matrix

**Configuration:**
- Rows: `Categories[Category]`
- Values: `[Total Sales]`

**Expected Grand Total:** 15,071,900.07

**Business Purpose:** Identify the sales contribution of each product category and understand category-level revenue performance.

**Status:** Completed

### Task 2 — Sales by Store

**Objective:** Compare sales performance across different stores.

**Power BI Visual:** Matrix

**Configuration:**
- Rows: `Stores[StoreName]`
- Values: `[Total Sales]`

**Expected Grand Total:** 15,071,900.07

**Business Purpose:** Identify high-performing and low-performing stores and compare their contribution to overall revenue.

**Status:** Completed

### Task 3 — Monthly Sales Trend

**Objective:** Analyse monthly sales trends and identify changes in sales performance over time.

**Power BI Visual:** Line Chart

**Configuration:**
- X-axis: `DateTable[Year-Month]`
- Y-axis: `[Total Sales]`

**Period:** January 2022 – December 2025

**Business Purpose:** Understand monthly sales patterns, identify trends and support business planning.

**Status:** Completed