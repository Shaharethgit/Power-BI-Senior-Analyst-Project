# DAX Measures Documentation

## 1. Basic Business Measures

### Total Sales
```dax
Total Sales = SUM(Sales[NetSales])
```

### Total Quantity
```dax
Total Quantity = SUM(Sales[Quantity])
```

### Total Orders
```dax
Total Orders = DISTINCTCOUNT(Sales[OrderID])
```

### Total COGS
```dax
Total COGS = SUM(Sales[COGS])
```

### Gross Profit
```dax
Gross Profit = SUM(Sales[GrossProfit])
```

### Gross Margin %
```dax
Gross Margin % = DIVIDE([Gross Profit], [Total Sales])
```

### Total Returns
```dax
Total Returns = SUM(Returns[ReturnValue])
```

### Net Revenue
```dax
Net Revenue = [Total Sales] - [Total Returns]
```

### Total Target
```dax
Total Target = SUM(MonthlyTargets[SalesTarget])
```

### Target Achievement %
```dax
Target Achievement % = DIVIDE([Total Sales], [Total Target])
```

## 2. Time Intelligence Measures

### Last Year Sales
```dax
Last Year Sales =
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR(DateTable[Date])
)
```

### Sales YoY Growth %
```dax
Sales YoY Growth % =
VAR LS = CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR(DateTable[Date])
)
VAR gowth = [Total Sales] - LS
RETURN
    IF([Total Sales] = BLANK(), BLANK(), DIVIDE(gowth, LS))
```

### Previous Month Sales
```dax
Previous Month Sales =
CALCULATE(
    [Total Sales],
    DATEADD(DateTable[Date], -1, MONTH)
)
```

### MoM Growth %
```dax
MoM Growth % =
VAR momgrowth = [Total Sales] - [Previous Month Sales]
RETURN
    DIVIDE(momgrowth, [Previous Month Sales])
```

### YTD Sales
```dax
YTD Sales =
TOTALYTD(
    [Total Sales],
    DateTable[Date]
)
```

### QTD Sales
```dax
QTD Sales =
TOTALQTD(
    [Total Sales],
    DateTable[Date]
)
```

### MTD Sales
```dax
MTD Sales =
TOTALMTD(
    [Total Sales],
    DateTable[Date]
)
```

### Rolling 3-Month Sales
```dax
Rolling 3-Month Sales =
CALCULATE(
    [Total Sales],
    DATESINPERIOD(
        DateTable[Date],
        MAX(DateTable[Date]),
        -3,
        MONTH
    )
)
```

### Rolling 6-Month Sales
```dax
Rolling 6-Month Sales =
CALCULATE(
    [Total Sales],
    DATESINPERIOD(
        DateTable[Date],
        MAX(DateTable[Date]),
        -6,
        MONTH
    )
)
```

### Rolling 12-Month Sales
```dax
Rolling 12-Month Sales =
CALCULATE(
    [Total Sales],
    DATESINPERIOD(
        DateTable[Date],
        MAX(DateTable[Date]),
        -12,
        MONTH
    )
)
```

### Same Period Last Year (SPLY) Sales
```dax
Same Period Last Year (SPLY) Sales =
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR(DateTable[Date])
)
```

## 3. Notes

- `CALCULATE` modifies filter context.
- `SAMEPERIODLASTYEAR` compares the current period with the equivalent previous-year period.
- `DATEADD` shifts the date context.
- `TOTALYTD`, `TOTALQTD`, and `TOTALMTD` calculate cumulative sales.
- `DATESINPERIOD` creates rolling date periods.
- `DIVIDE` safely handles division by zero.