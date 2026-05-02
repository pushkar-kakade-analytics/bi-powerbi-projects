# Financial MIS Dashboard – Relationship Mapping

## Overview
The Financial MIS Dashboard follows a star schema-based modeling approach for scalable and efficient reporting.

The model is designed to support financial, operational, and project-level analytics.

---

# Tables Used

## Fact Table
- Fact_Financials

## Dimension Tables
- Dim_Date
- Dim_Project

---

# Relationship Design

## Relationship 1

### From
Dim_Date[Month_End_Date]

### To
Fact_Financials[Month_End_Date]

### Relationship Type
One-to-Many

### Cross Filter Direction
Single

### Purpose
Supports:
- Time intelligence calculations
- YTD and MTD reporting
- Monthly trend analysis
- Rolling calculations

---

## Relationship 2

### From
Dim_Project[Project_ID]

### To
Fact_Financials[Project_ID]

### Relationship Type
One-to-Many

### Cross Filter Direction
Single

### Purpose
Supports:
- Project-level reporting
- SBG/SBU/BU hierarchy analysis
- Customer analysis
- Region-wise reporting
- Project profitability tracking

---

# Modeling Best Practices Used

- Star schema design
- Single-direction filtering
- Dimension-to-fact filtering
- Avoidance of many-to-many relationships
- Centralized KPI calculations

---

# Reporting Benefits

This relationship structure enables:
- Scalable dashboard performance
- Simplified DAX calculations
- Better filtering behavior
- Reusable reporting logic
- Enterprise-grade analytics structure

---

# Portfolio Purpose

This model demonstrates practical data modeling approaches commonly used in enterprise Power BI implementations for financial MIS reporting.
