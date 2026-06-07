# Data Engineering & Preparation

Before analysis, several calculated fields were created to improve reporting accuracy and dashboard performance.

---

## Revenue_Clean

### Purpose

Standardize revenue values for aggregation.

### Business Need

Raw sales values often contain formatting inconsistencies and cannot always be used directly inside PivotTables.

### Result

A clean numeric field suitable for:

* Summation
* KPI calculations
* Revenue analysis
* PivotTable aggregation

---

## Order_Month

### Purpose

Create a monthly time hierarchy.

### Example Output

```text
2022-03
2022-04
2022-05
2022-06
```

### Usage

Used throughout:

* Monthly Revenue Trend
* Slicer Filtering
* Time-Series Analysis

---

## Order_Year

### Purpose

Support future yearly reporting and trend analysis.

### Example

```text
2022
```

---

## Order_Status_Group

### Purpose

Normalize order statuses into business-friendly reporting categories.

### Categories

```text
Shipped
Cancelled
Other
```

### Benefit

Simplifies fulfillment reporting.

---

# KPI Engineering

The dashboard calculates multiple performance indicators.

---

## KPI 1 — Total Revenue

### Definition

Total value generated from all completed sales.

### Calculation

```excel
SUM(Revenue_Clean)
```

### Result

₹78.59 Million+

### Business Value

Measures total business performance.

---

## KPI 2 — Total Orders

### Definition

Total transaction count.

### Calculation

```excel
COUNT(Order ID)
```

### Result

128,975 Orders

### Business Value

Measures sales volume.

---

## KPI 3 — Average Order Value (AOV)

### Definition

Average revenue generated per order.

### Calculation

```excel
Total Revenue ÷ Total Orders
```

### Formula Logic

```excel
=SUM(Revenue_Clean)/COUNT(Order_ID)
```

### Result

₹609.36

### Business Value

Measures customer spending behavior.

---

## KPI 4 — Cancellation Rate

### Definition

Percentage of orders cancelled.

### Calculation

```excel
Cancelled Orders ÷ Total Orders
```

### Formula Logic

```excel
=Cancelled Orders / Total Orders
```

### Result

14%

### Business Value

Measures operational efficiency.

---

# Pivot Table Architecture

The dashboard is powered entirely through PivotTables.

---

# Pivot Table 1 — Monthly Revenue Trend

### Configuration

Rows

```text
Order_Month
```

Values

```text
Sum of Revenue_Clean
```

### Purpose

Track sales performance over time.

### Output

| Month   | Revenue |
| ------- | ------- |
| 2022-03 | ₹1.06M  |
| 2022-04 | ₹28.84M |
| 2022-05 | ₹26.23M |
| 2022-06 | ₹23.43M |

### Insight

April generated the highest revenue while June showed a decline.

---

# Pivot Table 2 — Revenue by Category

### Configuration

Rows

```text
Category
```

Values

```text
Sum of Revenue_Clean
```

### Purpose

Evaluate category contribution.

### Output

Categories analyzed:

* Set
* Kurta
* Western Dress
* Top
* Saree
* Dupatta
* Bottom
* Blouse
* Ethnic Dress

### Insight

Revenue is concentrated within a small number of product categories.

---

# Pivot Table 3 — Order Status Distribution

### Configuration

Rows

```text
Order_Status_Group
```

Values

```text
Count of Order ID
```

### Purpose

Evaluate fulfillment outcomes.

### Output

| Status    | Orders  |
| --------- | ------- |
| Shipped   | 109,696 |
| Cancelled | 18,332  |
| Other     | 947     |

### Insight

The fulfillment process is highly successful, though cancellations remain a measurable concern.

---

# Pivot Table 4 — Revenue by State

### Configuration

Rows

```text
Ship State
```

Values

```text
Sum of Revenue_Clean
```

### Purpose

Analyze geographic sales performance.

### Insight

Revenue concentration is highly uneven across states, indicating market-specific demand patterns.

---

# Pivot Table 5 — B2B Revenue Analysis

### Configuration

Rows

```text
B2B
```

Values

```text
Sum of Revenue_Clean
```

### Purpose

Compare wholesale versus retail activity.

### Output

| Customer Type | Revenue |
| ------------- | ------- |
| FALSE         | ₹78.0M  |
| TRUE          | ₹591K   |

### Insight

Revenue is overwhelmingly generated from non-B2B customers.

---

# Preview

