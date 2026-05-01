# Financial MIS Dashboard – Data Model

## Overview
The Financial MIS Dashboard uses a star schema-based data model designed for scalable and efficient business reporting.

The model separates transactional data from descriptive business dimensions to improve reporting performance and maintainability.

---

# Fact Table

## Fact_Financials

This is the primary transactional table containing financial and operational KPI data.

### Columns
- Date
- Business_Unit
- Region
- Customer_Segment
- Revenue_Actual
- Revenue_AOP
- Expense
- Profit

### Purpose
The fact table stores measurable business metrics used for reporting and analysis.

---

# Dimension Tables

## Dim_Date

Calendar dimension used for time-based reporting.

### Columns
- Date
- Month
- Quarter
- Year
- Month_Number
- Financial_Year

### Purpose
Supports:
- YTD reporting
- MTD reporting
- Trend analysis
- Time intelligence calculations

---

## Dim_Business_Unit

Business hierarchy dimension table.

### Columns
- Business_Unit
- SBU
- Segment
- Region

### Purpose
Supports:
- Business unit analysis
- Segment-level reporting
- Regional performance comparison

---

# Data Modeling Approach

## Recommended Design
- Star schema model
- Single-direction relationships
- One-to-many relationships

## Benefits
- Improved report performance
- Simplified DAX calculations
- Better scalability
- Easier maintenance

---

# Reporting Capabilities Enabled

This data model supports:
- Actual vs AOP analysis
- Variance calculations
- YTD and MTD reporting
- Business unit contribution analysis
- Trend and performance monitoring

---

# Portfolio Purpose

This data model demonstrates enterprise BI modeling practices commonly used in financial and management reporting systems.
