# Financial MIS Dashboard – Power BI Data Model Build Strategy

## Overview
This document defines the Power BI data model implementation strategy for the Financial MIS Dashboard.

The objective is to build a scalable, optimized, and enterprise-grade semantic model that supports executive reporting, financial analysis, and project-level analytics.

---

# Data Sources

## Planned Source Files
- Dim_Project.csv
- Dim_Date.csv
- Fact_Financials.csv

## Data Source Type
Flat-file CSV-based source system used for portfolio simulation purposes.

---

# Data Model Architecture

## Modeling Approach
Star schema design.

## Fact Table
- Fact_Financials

## Dimension Tables
- Dim_Date
- Dim_Project

---

# Fact Table Design

## Fact_Financials

### Granularity
One row per project per month.

### Business Grain
Monthly project-level financial snapshot.

### Key Purpose
Stores all measurable financial and operational KPIs used for reporting and analysis.

---

# Dimension Table Design

## Dim_Date

### Purpose
Supports:
- YTD calculations
- MTD reporting
- Trend analysis
- Financial year reporting

### Recommended Hierarchy
- Financial Year
- Quarter
- Month

---

## Dim_Project

### Purpose
Supports:
- Business hierarchy analysis
- Region-wise reporting
- Customer analysis
- Project governance reporting

### Recommended Hierarchy
- SBG
- SBU
- BU
- Project_Name

---

# Relationship Design

## Relationship 1

### From
Dim_Date[Month_End_Date]

### To
Fact_Financials[Month_End_Date]

### Type
One-to-Many

### Filter Direction
Single

---

## Relationship 2

### From
Dim_Project[Project_ID]

### To
Fact_Financials[Project_ID]

### Type
One-to-Many

### Filter Direction
Single

---

# Data Model Optimization Strategy

## Recommended Practices
- Use integer/surrogate keys where possible
- Hide technical columns from report view
- Avoid unnecessary calculated columns
- Use measures instead of calculated columns
- Keep relationships simple
- Maintain star schema structure

---

# Hidden Columns Recommendation

## Recommended Hidden Columns
- Project_ID
- Month_End_Date
- Technical helper columns

## Purpose
Improve report usability and reduce visual clutter.

---

# Formatting Standards

## Currency Fields
- INR format
- Thousand separator enabled
- Lakhs/Crores display formatting where required

## Percentage Fields
- Two decimal precision

## Date Fields
- Consistent month-year formatting

---

# Hierarchy Planning

## Date Hierarchy
Financial Year
→ Quarter
→ Month

## Business Hierarchy
SBG
→ SBU
→ BU
→ Project_Name

---

# Model Validation Checklist

## Validation Areas
- Relationship correctness
- Duplicate key validation
- Null value validation
- KPI reconciliation
- Granularity validation
- Financial total validation

---

# Scalability Planning

The data model is designed to support future expansion for:
- Daily reporting
- Forecasting models
- Budget planning
- Department-level reporting
- Drill-through analytics

---

# Reporting Capabilities Enabled

This semantic model supports:
- Executive MIS reporting
- Financial analysis
- Actual vs AOP reporting
- Profitability analysis
- Working capital monitoring
- Project-level analytics
- Enterprise KPI reporting

---

# Portfolio Purpose

This document demonstrates enterprise-grade Power BI semantic model planning and implementation practices commonly used in large-scale business intelligence solutions.
