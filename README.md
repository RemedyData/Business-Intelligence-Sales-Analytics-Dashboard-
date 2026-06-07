# Amazon Sales Analytics Dashboard

### Excel Business Intelligence, Sales Analytics & Interactive Reporting Solution

---

# Project Overview

The Amazon Sales Analytics Dashboard is a comprehensive Excel-based Business Intelligence solution developed to transform raw Amazon transactional data into a centralized decision-support system.

The project integrates data transformation, KPI engineering, PivotTable architecture, interactive filtering, sales analytics, and dashboard visualization techniques to enable business users to analyze revenue performance, fulfillment efficiency, customer behavior, geographic distribution, and product-category performance from a single reporting environment.

The solution was built entirely in Microsoft Excel using structured datasets, calculated fields, PivotTables, slicers, KPI calculations, and dashboard design principles.

---

# Business Problem

Large transactional datasets are difficult to interpret directly.

Stakeholders often need answers to questions such as:

* How much revenue are we generating?
* Which products drive the majority of sales?
* Which states generate the highest revenue?
* What percentage of orders are cancelled?
* Are sales improving over time?
* What is the average value of each order?
* How do B2B customers compare with retail customers?

Raw transactional data alone cannot answer these questions efficiently.

The objective of this project was to convert raw sales transactions into actionable business intelligence through interactive reporting and visualization.

---

# Project Objectives

The dashboard was developed to:

* Monitor overall sales performance
* Track monthly revenue trends
* Analyze category-level sales contribution
* Evaluate order fulfillment outcomes
* Measure cancellation rates
* Compare B2B vs Retail performance
* Analyze state-wise revenue distribution
* Enable dynamic filtering through slicers
* Provide executive-level KPI reporting

---

# Dataset Overview

The source dataset contains Amazon sales transactions.

Each row represents a unique order transaction.

The dataset includes:

### Order Attributes

* Order ID
* Order Date
* Order Status
* Fulfillment Type
* Sales Channel
* Shipping Service

### Product Attributes

* SKU
* Product Style
* Product Category
* Product Size
* ASIN

### Geographic Attributes

* Ship City
* Ship State
* Postal Code
* Country

### Sales Attributes

* Quantity
* Currency
* Amount

### Customer Attributes

* B2B Flag
* Fulfilled By

---

# Workbook Architecture

```text
Amazon Sales Analytics Dashboard
│
├── Amazon Sale Report
│      Raw Data Layer
│
├── Pivot_Tables
│      Aggregation & Calculation Layer
│
└── Dashboard
       Reporting & Visualization Layer
```

# Validation & Quality Assurance

The following validation checks were performed:

### Revenue Reconciliation

Verified dashboard revenue equals raw data revenue.

---

### Pivot Validation

Confirmed PivotTable totals match source records.

---

### Slicer Testing

Validated all slicers update connected PivotTables correctly.

---

### KPI Verification

Cross-checked KPI values against source calculations.

---

### Duplicate Review

Verified transaction uniqueness.

---

# Challenges Encountered

## Challenge 1

Large transaction dataset slowed dashboard responsiveness.

### Solution

Used PivotTables instead of worksheet formulas for aggregation.

---

## Challenge 2

Revenue calculations required standardization.

### Solution

Created Revenue_Clean field.

---

## Challenge 3

Multiple reporting dimensions complicated dashboard design.

### Solution

Implemented centralized slicer architecture.

---

## Challenge 4

Business users required simplified reporting.

### Solution

Designed KPI-driven executive dashboard.

---

# Future Enhancements

Potential future upgrades include:

* Customer Cohort Analysis
* Repeat Purchase Analysis
* Customer Lifetime Value (CLV)
* RFM Segmentation
* Forecasting Models
* Power Query Automation
* Power Pivot Data Model
* Geographic Heat Maps
* Inventory Analytics

---

# Technologies Used

* Microsoft Excel
* Excel Tables
* PivotTables
* PivotCharts
* Slicers
* Structured References
* Conditional Formatting
* Dashboard Design
* Business Intelligence Reporting

---

# Skills Demonstrated

* Data Cleaning
* Data Transformation
* Sales Analytics
* Dashboard Design
* KPI Development
* Pivot Table Engineering
* Business Intelligence
* Data Visualization
* Geographic Analysis
* Executive Reporting
* Excel Automation
* Business Storytelling

---

# Tags

#Excel
#SalesAnalytics
#AmazonSales
#BusinessIntelligence
#DashboardDesign
#PivotTables
#DataVisualization
#DataAnalysis
#Reporting
#KPIAnalysis
#MicrosoftExcel
#BusinessAnalytics
#InteractiveDashboard
#PortfolioProject
#DataStorytelling
#RetailAnalytics
#EcommerceAnalytics
#ExcelDashboard
#DataDrivenDecisionMaking
