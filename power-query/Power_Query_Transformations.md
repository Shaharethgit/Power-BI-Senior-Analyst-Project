# Power Query Transformations

## 1. Overview

Power Query was used to inspect, prepare, and validate the retail dataset before building the Power BI data model.

## 2. Data Inspection

- Reviewed available tables and columns.
- Inspected column data types.
- Checked table structures and row counts.
- Identified fact and dimension tables.

## 3. Data Quality Checks

Performed validation checks for:

- Missing values
- Duplicate records
- Primary key uniqueness
- Foreign key consistency
- Invalid data types
- Fact-table grain
- Monthly target uniqueness

## 4. Data Modelling Preparation

Prepared the tables for relationships between fact and dimension tables.

Key preparation areas:

- Identifying primary and foreign keys.
- Checking duplicate key combinations.
- Understanding one-to-many relationships.
- Validating the grain of fact tables.

## 5. Query Merging

Practised different merge operations:

- Left Outer Join
- Inner Join
- Left Anti Join

These operations help combine tables and identify unmatched records.

## 6. Python Integration with Pandas

Explored Python integration through the Power Query Run Python Script feature.

Key concepts:

- Using the selected query as the `dataset` DataFrame.
- Inspecting and transforming data using Pandas.
- Cleaning category values.
- Understanding how to work with other source tables.
- Merging datasets using Pandas `merge()`.

Example:

```python
import pandas as pd

df = dataset

df["Category"] = df["Category"].str.strip()
```

## 7. Outcome

The preparation and validation process helped establish a reliable foundation for data modelling, DAX calculations, and business analysis.