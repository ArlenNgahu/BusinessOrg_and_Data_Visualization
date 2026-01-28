# Power BI Sales Dashboard (Built-in Visuals Only)

## Author
Arlen Ngahu  
Data Science Student  

## Project Overview
This project demonstrates the creation of an interactive sales dashboard using **Power BI Desktop** while strictly relying on **built-in visuals and automatic aggregations** (Sum, Count, Average).  
No DAX formulas, calculated columns, or data transformations were used.

The goal was to load an existing Excel dataset, explore the data visually, and present key business insights through a clean, professional, and interactive dashboard.

The link to the Power BI dashboard is : (https://app.powerbi.com/groups/me/reports/58090d0c-c5f5-47c7-9eb7-16e79f46fce8/05682f87e5c728c3224a?experience=power-bi)

## Project Overview
This project demonstrates the creation of an interactive sales dashboard using **Power BI Desktop** while strictly relying on **built-in visuals and automatic aggregations** (Sum, Count, Average).  
No DAX formulas, calculated columns, or data transformations were used.

The goal was to load an existing Excel dataset, explore the data visually, and present key business insights through a clean, professional, and interactive dashboard.

---

## Objectives
- Load data correctly into Power BI Desktop  
- Select appropriate visuals for different data types  
- Use only automatic summarization (no custom calculations)  
- Build an interactive dashboard with slicers  
- Apply professional formatting and layout  
- Publish report to Power BI Service and create a dashboard  

---

## Dataset Information
**File:** `Sales_Data.xlsx`  
**Sheet:** `Sales`

**Columns:**
- Date (Date)
- Region (Text)
- Country (Text)
- Product Category (Text)
- Product (Text)
- Salesperson (Text)
- Units Sold (Number)
- Unit Price (Number)
- Revenue (Number – pre-calculated)

---

## Tools Used
- Power BI Desktop  
- Microsoft Excel (data source)  
- Power BI Service (publishing & dashboard pinning)

---

## Data Loading Process
1. Open Power BI Desktop  
2. Click **Get Data → Excel**  
3. Select `Sales_Data.xlsx`  
4. Choose **Sales** sheet  
5. Click **Load** (no Transform Data)

---

## Dashboard Visuals

| # | Visual | Fields Used | Aggregation |
|--|-------|-------------|-------------|
|1|Card – Total Revenue|Revenue|Sum|
|2|Card – Total Units Sold|Units Sold|Sum|
|3|Card – Average Unit Price|Unit Price|Average|
|4|Clustered Column – Revenue by Region|Region, Revenue|Sum|
|5|Bar Chart – Revenue by Country|Country, Revenue|Sum|
|6|Donut Chart – Revenue by Product Category|Product Category, Revenue|Sum|
|7|Bar Chart – Top 5 Products by Revenue|Product, Revenue|Top N (5)|
|8|Line Chart – Sales Trend Over Time|Date (Month), Revenue|Sum|
|9|Stacked Column – Units Sold by Salesperson|Salesperson, Units Sold|Sum|
|10|Table – Detailed Sales|Date, Region, Product, Salesperson, Revenue|Default|

---

## Interactivity
Three slicers were added:
- Region  
- Product Category  
- Date (Between)

All visuals respond dynamically to slicer selections.

---

## Formatting & Layout
- Applied a custom JSON theme  
- Aligned visuals using grid layout  
- Removed unnecessary borders  
- Used consistent font sizes  
- Organized visuals into logical sections (KPIs, Trends, Products, Geography)

---

## Publishing
1. Signed into Power BI Desktop  
2. Clicked **Home → Publish → My workspace**  
3. Opened report in Power BI Service  
4. Pinned visuals to create a dashboard  

---

## Key Insights
- Revenue and units sold vary significantly by region and country  
- Certain product categories contribute more heavily to overall revenue  
- A small number of products generate the highest revenue (Top 5)  
- Sales fluctuate across months, indicating possible seasonality  
- High-performing salespersons can be identified for benchmarking  

---

## Outcome
The final result is a fully interactive Power BI dashboard that provides a clear overview of sales performance and supports data-driven decision-making without using advanced calculations.

---

