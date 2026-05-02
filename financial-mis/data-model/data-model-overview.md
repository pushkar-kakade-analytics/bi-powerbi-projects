# Financial MIS Dashboard – Data Model

## Overview
The Financial MIS Dashboard uses a star schema-based data model designed for scalable and efficient enterprise reporting.

The model is structured to support financial, operational, and project-level analysis for a large construction and infrastructure organization.

The reporting approach is project-centric, enabling detailed monitoring of business performance across multiple regions, business units, and project categories.

---

# Fact Table

## Fact_Financials

This is the primary transactional table containing financial and operational KPI data.

### Columns
- Date
- Project_ID
- Revenue_Actual
- Revenue_AOP
- Expense
- Profit
- Billing
- Collection
- Cashflow

### Purpose
The fact table stores measurable business metrics used for:
- Financial reporting
- KPI monitoring
- Variance analysis
- Cashflow tracking
- Project profitability analysis

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

## Dim_Project

Project-level dimension table used for business hierarchy and operational reporting.

### Columns
- Project_ID
- Project_Name
- SBG
- SBU
- BU
- Customer_Name
- Project_Type
- Project_Scope
- Project_Status
- Project_Manager
- Project_Location
- Region
- Contract_Value
- Project_Priority
- Execution_Mode
- Start_Date
- End_Date

### Purpose
Supports:
- Project-level financial reporting
- Business hierarchy analysis
- Customer reporting
- Active vs closed project tracking
- Project profitability analysis
- Regional performance monitoring
- Contract value analysis
- Executive MIS reporting

---

# Data Modeling Approach

## Recommended Design
- Star schema model
- Single-direction relationships
- One-to-many relationships
- Project-centric reporting structure

## Benefits
- Improved report performance
- Simplified DAX calculations
- Better scalability
- Easier maintenance
- Standardized KPI reporting

---

# Reporting Capabilities Enabled

This data model supports:
- Actual vs AOP analysis
- Variance calculations
- YTD and MTD reporting
- Project profitability tracking
- Revenue trend analysis
- Region-wise reporting
- SBG/SBU/BU hierarchy analysis
- Cashflow monitoring
- Executive-level KPI reporting

---

# Portfolio Purpose

This data model demonstrates enterprise BI modeling practices commonly used in construction, infrastructure, and project-driven organizations.

The project is intended to showcase:
- Financial reporting capability
- Business intelligence architecture
- Data modeling expertise
- KPI framework design
- Enterprise dashboard planning
