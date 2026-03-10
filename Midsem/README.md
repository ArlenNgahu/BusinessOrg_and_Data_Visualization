#  Global Superstore Business Intelligence Dashboard

In this project, I built a complete **Business Intelligence solution using Microsoft Power BI**, where I transformed raw retail transaction data into a **clean star-schema data model and interactive analytical dashboard**.

My goal was to demonstrate the **full BI workflow**, from data cleaning to visualization and cloud publishing, while following professional data modelling practices used in real-world analytics projects.



#  Project Overview

For this project, I followed a structured Business Intelligence pipeline:

1. I obtained the dataset
2. I cleaned and transformed the data using **Power Query**
3. I designed a **star schema data model**
4. I created an **interactive Power BI dashboard**
5. I published the report to **Power BI Service**

By completing these steps, I was able to convert raw transactional data into **clear visual insights that support business decision-making**.



#  Dataset

For this project, I used the **Global Superstore Sales Dataset**, which is a commonly used dataset for learning business intelligence and data analytics.

### Dataset Characteristics

The dataset contains:

* Thousands of retail sales transactions
* Product categories and subcategories
* Customer segmentation data
* Geographic information such as region, country, state, and city
* Order dates suitable for time-based analysis
* Key sales metrics including **Sales, Profit, and Quantity**

This dataset allowed me to explore **customer behaviour, regional sales performance, and product trends**.



## Dataset Source

![alt text](screenshots/image.png)

```
screenshots/dataset_source.png
```


#  Data Preparation (Power Query)

Before building the dashboard, I first cleaned and prepared the dataset using **Power Query Editor in Power BI**.

Data preparation is important because raw datasets usually contain inconsistencies, duplicates, or unnecessary columns that can affect analysis.

### Cleaning Steps I Performed

During the data cleaning stage, I:

* Removed duplicate records
* Fixed incorrect data types
* Standardized text formatting
* Removed unnecessary columns
* Renamed columns for clarity
* Trimmed and cleaned text fields
* Checked for null or missing values

These steps helped ensure that the dataset was **consistent, accurate, and ready for modelling**.



## Power Query Editor

![alt text](screenshots/image-1.png)
![alt text](screenshots/image-2.png)
![alt text](screenshots/image-3.png)

```
screenshots/powerquery_editor.png
```


## Applied Transformations

Power BI keeps track of all cleaning steps in the **Applied Steps panel**, which allows transformations to be easily reproduced and audited.

![alt text](screenshots/image-4.png)
![alt text](screenshots/image-5.png)
![alt text](screenshots/image-6.png)
![alt text](screenshots/image-7.png)
![alt text](screenshots/image-8.png)
![alt text](screenshots/image-9.png)
![alt text](screenshots/image-10.png)
![alt text](screenshots/image-11.png)
![alt text](screenshots/image-12.png)
![alt text](screenshots/image-13.png)
![alt text](screenshots/image-14.png)
![alt text](screenshots/image-15.png)
![alt text](screenshots/image-16.png)
![alt text](screenshots/image-17.png)
![alt text](screenshots/image-18.png)
![alt text](screenshots/image-19.png)
![alt text](screenshots/image-20.png)
![alt text](screenshots/image-21.png)
![alt text](screenshots/image-22.png)


```
screenshots/applied_steps.png
```




#  Geographic Key Engineering

While preparing the data, I noticed that the dataset did **not include a unique identifier for geographic regions**.

Because a star schema requires unique keys for relationships, I decided to create a **RegionID**.

To generate this identifier, I combined several geographic attributes:

* Region
* Country
* State
* City

Using these fields, I created a **composite key** and then generated a surrogate key called **RegionID**.

This ensured that each geographic location could be uniquely identified and properly linked within the model.



## RegionID Creation

![alt text](screenshots/image-23.png)

```
screenshots/region_key_creation.png
```





#  Query Dependencies

To better understand how my queries were structured, I used **Power BI's Query Dependencies view**.

This view helped me confirm that my dimension tables were properly created before being used by the **FactSales table**.

![alt text](screenshots/image-24.png)
![alt text](screenshots/image-25.png)
![alt text](screenshots/image-26.png)
![alt text](screenshots/image-27.png)
![alt text](screenshots/image-28.png)
![alt text](screenshots/image-29.png)
![alt text](screenshots/image-30.png)
![alt text](screenshots/image-31.png)
![alt text](screenshots/image-32.png)


```
screenshots/query_dependencies.png
```




#  Data Modelling — Star Schema

After cleaning the data, I designed a **star schema**, which is a common data modelling technique used in data warehouses and BI systems.

A star schema improves:

* Query performance
* Data organization
* Analytical clarity

My model contains one **fact table** connected to several **dimension tables**.



## Fact Table

### FactSales

This table contains the **main transactional data**, including:

* Sales
* Profit
* Quantity
* Order Date
* Foreign keys linking to dimension tables

Fact tables store the **measurable business metrics** that are analyzed in dashboards.



## Dimension Tables

I created several dimension tables to describe the context of the sales data.

| Dimension       | Description                                               |
| --------------- | --------------------------------------------------------- |
| **DimDate**     | Contains time attributes such as year, month, and quarter |
| **DimProduct**  | Contains product categories and subcategories             |
| **DimCustomer** | Contains customer segment information                     |
| **DimRegion**   | Contains geographic information                           |

Dimension tables provide **descriptive attributes used for filtering and grouping data**.


## Star Schema Model

![alt text](screenshots/image-33.png)
![alt text](screenshots/image-34.png)
![alt text](screenshots/image-35.png)
![alt text](screenshots/image-36.png)
![alt text](screenshots/image-37.png)
![alt text](screenshots/image-38.png)
![alt text](screenshots/image-39.png)


```
screenshots/star_schema_model.png
```



#  Dashboard Development

After completing the data model, I created an **interactive Power BI dashboard** to visualize the insights contained in the dataset.

My goal was to design a dashboard that could help users quickly understand:

* overall sales performance
* regional performance
* product trends
* customer segment behaviour



#  Dashboard Visualizations

The dashboard includes several visuals:

### Key Performance Indicators

To summarize the overall performance, I created KPI cards showing:

* Total Sales
* Total Profit
* Total Quantity Sold
* Average Sales



### Sales Trend Over Time

I created a **line chart** showing how sales change over time.
This allows users to easily identify **seasonal trends and growth patterns**.



### Sales by Product Category

A **bar chart** was used to compare sales across different product categories.

This visualization helps highlight **which product categories generate the most revenue**.

---

### Sales by Region

A **regional chart** was created to show how sales vary across geographic regions.

This makes it easier to identify **strong and weak markets**.

---

### Customer Segment Distribution

A visual was also created to show how sales are distributed across different **customer segments**.



# 📊 Final Dashboard

![alt text](screenshots/image-40.png)
![alt text](screenshots/image-41.png)
![alt text](screenshots/image-42.png)


```
screenshots/dashboard_overview.png
```





#  KPI Overview

![alt text](screenshots/image-43.png)

```
screenshots/dashboard_kpis.png
```





#  Deployment (Power BI Service)

After finishing the report, I published it to **Power BI Service** so that it could be accessed online.

Publishing the dashboard allows users to:

* view the report from anywhere
* share dashboards with others
* integrate analytics into web platforms



![alt text](screenshots/image-44.png)
![alt text](screenshots/image-45.png)

## Published Dashboard

![alt text](screenshots/image-46.png)
![alt text](screenshots/image-47.png)
![alt text](screenshots/image-48.png)
```
screenshots/powerbi_service_dashboard.png
```




#  Live Dashboard

You can view the interactive dashboard here:

https://app.powerbi.com/view?r=eyJrIjoiOWU4ZjZiZTAtODUyZS00NDc5LWJlOTItMGY0ZDFhYmQwYTU5IiwidCI6IjE2ZDgzZWU2LTI1NGEtNDY5ZC1hNmNjLTU0ZTJjYTIzMTNlNyIsImMiOjh9


#  Project Structure

```
PowerBI-Sales-Analytics-Dashboard
│
├── README.md
├── Global_Superstore_BI_Report.pdf
├── superstore_dashboard.pbix
│
└── screenshots
    ├── dataset_source.png
    ├── powerquery_editor.png
    ├── applied_steps.png
    ├── region_key_creation.png
    ├── query_dependencies.png
    ├── star_schema_model.png
    ├── dashboard_overview.png
    ├── dashboard_kpis.png
    └── powerbi_service_dashboard.png
```



#  Skills Demonstrated

Through this project, I demonstrated several Business Intelligence skills:

* Data cleaning using Power Query
* Dimensional modelling
* Star schema design
* Dashboard development
* Data storytelling
* Interactive filtering
* Cloud publishing using Power BI Service


#  What I Learned

Through this project, I gained practical experience in transforming raw data into **structured analytical insights**.

I also learned how important **data modelling and data preparation** are for building effective dashboards.

These techniques are widely used in **modern business intelligence and analytics environments**.

---

#  Author

**Arlen Wambugu**

Business Intelligence & Data Visualization
Power BI | Data Analytics | Dashboard Development
