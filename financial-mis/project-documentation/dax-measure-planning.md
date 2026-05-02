# Financial MIS Dashboard – DAX Measure Planning

## Overview
This document defines the DAX measure planning strategy for the Financial MIS Dashboard.

The objective is to create a scalable, reusable, and enterprise-ready KPI framework that supports financial reporting, trend analysis, and executive MIS dashboards.

---

# DAX Design Principles

The following principles are followed during measure design:

- Reusable measure logic
- Consistent naming conventions
- Centralized KPI calculations
- Time intelligence standardization
- Performance-oriented calculations
- Business-friendly measure naming

---

# Measure Categories

The DAX measures are grouped into logical categories to improve maintainability and reporting consistency.

---

# 1. Base Measures

These are direct aggregations from the fact table.

## Planned Measures
- Revenue Actual
- Revenue AOP
- Project Cost
- Profit
- Billing
- Collection
- Cash Inflow
- Cash Outflow
- Accounts Receivable
- Accounts Payable

## Purpose
Base measures act as the foundation for all higher-level KPI calculations.

---

# 2. Variance Measures

Measures used for target comparison and performance analysis.

## Planned Measures
- Revenue Variance
- Revenue Variance %
- Profit Variance
- Profit Variance %

## Purpose
Supports Actual vs AOP analysis and executive performance reviews.

---

# 3. Profitability Measures

Measures focused on project financial performance.

## Planned Measures
- Profit Margin %
- Cost to Revenue Ratio
- Collection Efficiency %

## Purpose
Used for profitability tracking and operational efficiency analysis.

---

# 4. Time Intelligence Measures

Measures used for trend analysis and cumulative reporting.

## Planned Measures
- Revenue YTD
- Revenue MTD
- Profit YTD
- Billing YTD
- Rolling 3 Month Revenue
- Rolling 12 Month Revenue

## Purpose
Supports financial trend analysis and executive monthly reviews.

---

# 5. Cashflow Measures

Measures focused on liquidity and working capital monitoring.

## Planned Measures
- Net Cashflow
- Total AR
- Total AP
- AR to Revenue Ratio
- AP to Cost Ratio

## Purpose
Supports cashflow management and working capital analysis.

---

# Naming Convention Strategy

## Base Measures
Format:
[Metric Name]

Examples:
- [Revenue Actual]
- [Profit]
- [Billing]

---

## Derived Measures
Format:
[Metric Name] + Business Context

Examples:
- [Revenue Variance]
- [Profit Margin %]
- [Revenue YTD]

---

# Formatting Standards

## Currency Measures
- INR currency format
- Thousand separator enabled
- Display in Lakhs/Crores when required

## Percentage Measures
- Percentage format
- 2 decimal precision

## Ratio Measures
- Decimal format with 2 precision

---

# Performance Optimization Approach

The following best practices will be followed:

- Reuse base measures
- Avoid unnecessary calculated columns
- Minimize row context complexity
- Use variables for readability
- Standardize time intelligence calculations

---

# Reporting Capabilities Enabled

This DAX framework supports:
- Executive MIS reporting
- Actual vs AOP comparison
- Trend analysis
- Profitability monitoring
- Cashflow analysis
- Working capital tracking
- Project-level financial reporting

---

# Portfolio Purpose

This document demonstrates enterprise-grade DAX planning practices commonly followed in scalable Power BI implementations.
