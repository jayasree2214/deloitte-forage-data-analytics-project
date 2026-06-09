# deloitte-forage-data-analytics-project
# Deloitte Data Analytics Job Simulation | Forage

## Project Overview
This project was completed as part of the Deloitte Data Analytics Virtual Experience Program on Forage.

The objective was to analyze operational telemetry data collected from multiple manufacturing factories and generate insights to identify:
1. Which factory experienced the highest machine downtime.
2. Which machine types contributed most to downtime in that factory.

Additionally, a forensic analytics task was completed to evaluate employee compensation equality using classification logic.

---

## Business Problem

### Task 1 – Manufacturing Telemetry Analysis
Daikibo Industries collected telemetry data from manufacturing equipment across multiple global factories.

The business wanted to answer:

- Which factory experienced the most machine failures?
- Which machine categories contributed most to downtime?

The goal was to transform raw telemetry logs into actionable operational insights.

### Task 2 – Equality Investigation
Daikibo Industries wanted to investigate potential compensation inequality.

The objective was to classify equality scores and identify areas that may indicate unfair compensation patterns.

---

## Dataset Information

### Telemetry Dataset
- Data format: JSON
- Time period: May 2021 (1 month)
- Factories analyzed: 4
- Machine categories: 9
- Machine signals collected every 10 minutes

Factory locations:
- Tokyo, Japan
- Osaka, Japan
- Berlin, Germany
- Shenzhen, China

### Equality Dataset
Columns:
- Factory
- Job Role
- Equality Score (-100 to +100)

---

## Tools Used

- Tableau
- Microsoft Excel
- Data Visualization
- Calculated Fields
- Dashboard Design
- Data Analysis

---

# Task 1 — Telemetry Data Analysis

## Approach

### Data Preparation
- Imported JSON telemetry data into Tableau
- Explored machine health status records
- Prepared fields for downtime calculation

### Calculated Metric
Created a calculated measure:

Unhealthy =
IF [Status] = "Unhealthy"
THEN 10
ELSE 0
END

This represented:
- 10 minutes of potential downtime for each unhealthy machine event

---

## Dashboard Development

Created:

### 1. Down Time per Factory
- Bar chart
- Compared downtime across all factories

### 2. Down Time per Device Type
- Bar chart
- Displayed machine-level contribution to downtime

### Dashboard Features
- Interactive filtering
- Drill-down from factory → machine category
- Comparative downtime analysis

---

## Key Skills Demonstrated

- Data cleaning
- Calculated measures
- KPI creation
- Dashboard development
- Root cause analysis
- Interactive visualization

---

# Task 2 — Equality Classification Analysis

## Objective

Classify employee equality scores into business categories.

Classification Rules:

| Equality Score | Classification |
|---------------|---------------|
| -10 to +10 | Fair |
| <-10 or >10 | Unfair |
| <-20 or >20 | Highly Discriminative |

---

## Excel Logic

Example:

```excel
=IF(ABS(C2)<=10,"Fair",
IF(ABS(C2)<=20,"Unfair",
"Highly Discriminative"))
```

---

## Key Skills Demonstrated

- Business rule implementation
- Excel formula design
- Classification logic
- Data transformation

---

## Project Outcomes

- Converted raw telemetry records into measurable downtime metrics.
- Built interactive dashboards to support operational decision-making.
- Applied business rules to evaluate compensation equality.
- Delivered insights through clear and structured visual reporting.

---

## Project Learnings

Through this simulation, I learned:
- How business problems are translated into analytical workflows
- Dashboard design principles in Tableau
- Creating calculated fields and KPIs
- Converting raw data into business insights
- Applying rule-based classification in Excel

---

## Author

Jayasree  
Aspiring Data Analyst  
Skills: SQL | Excel | Tableau | Power BI | Python
