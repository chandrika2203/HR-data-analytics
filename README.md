# HR Analytics Dashboard

## Project Overview
The HR Analytics Dashboard is an interactive Power BI project designed to analyze employee data and provide insights into workforce performance, attrition, promotion eligibility, retrenchment analysis, job satisfaction, overtime trends, and departmental performance.

This dashboard helps HR teams and management make data-driven decisions by identifying employee trends, improving workforce planning, and monitoring key HR metrics.

---

# Tools & Technologies Used

- Power BI
- Power Query
- DAX (Data Analysis Expressions)
- Excel
- Data Visualization
- Data Cleaning & Transformation

---

# KPIs Used in Dashboard

## Employee KPIs
- Total Employees
- Male Employees
- Female Employees
- Gender Ratio

## Attrition KPIs
- Total Attrition Count
- Attrition Rate %
- Department-wise Attrition
- Job Role-wise Attrition

## Promotion KPIs
- Employees Due for Promotion
- Department-wise Promotion Analysis
- Promotion Eligible Employees

## Retrenchment KPIs
- Employees Due for Retrenchment
- Employees in Both Promotion & Retrenchment Categories

## Performance KPIs
- High Performance Rate
- Low Performance Rate
- Job Satisfaction Level

## Overtime KPIs
- Employees Working Overtime
- Overtime vs Attrition Analysis

---

# Important DAX Measures

## Total Employees
```DAX
Total Employees = COUNT(Employee[EmployeeNumber])
```

## Male Employees
```DAX
Male Employees =
CALCULATE([Total Employees], Employee[Gender] = "Male")
```

## Female Employees
```DAX
Female Employees =
CALCULATE([Total Employees], Employee[Gender] = "Female")
```

## Attrition Count
```DAX
Attrition Count =
CALCULATE([Total Employees], Employee[Attrition] = "Yes")
```

## Attrition Rate %
```DAX
Attrition Rate % =
DIVIDE([Attrition Count], [Total Employees], 0)
```

## Due for Promotion
```DAX
Due for Promotion =
CALCULATE(
    [Total Employees],
    Employee[Promotion Status] = "Due for Promotion"
)
```

## Retrenchment Count
```DAX
Retrenchment Count =
CALCULATE(
    [Total Employees],
    Employee[Retrenchment Status] = "Retrenchment"
)
```

## High Performance %
```DAX
High Performance % =
DIVIDE(
    CALCULATE(
        [Total Employees],
        Employee[Performance Rating] = "High"
    ),
    [Total Employees],
    0
)
```

---

# Dashboard Features

## Home Dashboard
- Overall workforce summary
- Employee distribution analysis
- Job satisfaction analysis
- Overtime analysis
- Department-wise promotion and retrenchment overview

## Action Dashboard
- Employees due for promotion
- Employees due for retrenchment
- Employees present in both promotion and retrenchment categories

## Detail Dashboard
- Gender-wise employee analysis
- Marital status analysis
- Monthly income comparison
- Job role analysis
- Attrition trends

---

# Key Insights

- Research & Development department has the highest number of employees.
- Employees working overtime show higher attrition rates.
- Sales Executives have comparatively higher attrition.
- Male employees represent 60% of the workforce.
- High-performance employees account for 85% of employees.
- Some employees appear in both promotion and retrenchment categories and require management review.

---

# Steps Performed

1. Collected HR employee dataset
2. Cleaned and transformed data using Power Query
3. Created calculated columns and DAX measures
4. Built KPIs and interactive visualizations
5. Added slicers, filters, and page navigation
6. Designed dashboard layout and reporting pages
7. Performed employee and departmental analysis

---

# Business Impact

This dashboard helps organizations to:
- Monitor employee performance
- Reduce attrition
- Improve workforce planning
- Identify promotion candidates
- Support strategic HR decision-making

---
