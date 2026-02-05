---
layout: page
title: Important Power BI Functions Explained
---

## Power BI Functions – Practical Guide

In this article, I explain some commonly used **Power BI (DAX) functions** with real-world usage.

---

### 🔹 CALCULATE()

`CALCULATE()` modifies the filter context of a measure.

**Example:**
```DAX
Total Sales YTD =
CALCULATE (
    [Total Sales],
    DATESYTD ( 'Calendar'[Date] )
)

When to use:

YTD / QTD calculations
Applying filters dynamically
Time intelligence scenarios
'''
---

### 🔹 Filter()
High Value Sales =
CALCULATE (
    [Total Sales],
    FILTER (
        Sales,
        Sales[Amount] > 10000
    )
)
