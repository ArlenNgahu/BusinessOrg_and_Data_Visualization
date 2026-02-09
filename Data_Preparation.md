Power BI Data Preparation & Transformation Report
Student Information
•	Name: Arlen Ngahu
•	ID Number: 667855
•	Course / Unit: Business Organization and Data Visualization
•	Lab / Task Number: DSA3050A
•	Date: 9/2/2026

1. Introduction
This report documents the complete data preparation and transformation process carried out in Power BI using Power Query Editor. The objective of this lab was to clean raw sales data, resolve data quality issues, create meaningful derived columns, and prepare the dataset for analysis and visualization.
The report explains:
•	Data loading and inspection
•	Locale and data type corrections
•	Handling errors in numerical columns (SalesAmount)
•	Creation and purpose of DataQualityFlag
•	Grouping data using multiple columns
•	Final validation of the dataset

2. Data Loading and Initial Inspection
The dataset was imported into Power BI using the Get Data option and opened in Power Query Editor for preprocessing.
Key actions performed:
•	Verified column names and data types
•	Identified columns with errors and inconsistent formats
•	Checked for null values and invalid entries
 
 ## Screenshot placeholder
 
 
3. Data Type and Locale Correction
Some numeric columns were incorrectly interpreted due to locale-specific formatting (for example, commas and decimal points).
Steps Followed:
1.	Selected the affected numeric column(s)
2.	Changed Data Type → Using Locale
3.	Set:
o	Data Type: Decimal Number or Whole Number
o	Locale: English (United States) (or appropriate locale)
This ensured numerical values were correctly parsed and reduced conversion errors.

 ## Screenshot placeholder
  


4. Handling Errors in SalesAmount
The SalesAmount column contained errors caused by:
•	Non-numeric values
•	Missing values
•	Incorrect formatting
Error Handling Approach:
•	Errors were replaced with nulls where appropriate
•	Rows with critical missing values were reviewed
•	Column was revalidated after corrections
This step ensured that aggregations and calculations would not fail during analysis.

 ## Screenshot placeholder

5. Creation of DataQualityFlag
To track the reliability of each row, a new column called DataQualityFlag was created.
Purpose of DataQualityFlag:
•	Indicates whether a record is Valid or Invalid
•	Helps identify rows affected by missing or erroneous data
•	Improves transparency and auditability of the dataset
Logic Used:
•	If SalesAmount is null or error → Invalid
•	Otherwise → Valid
This was implemented using a Conditional Column in Power Query.
 
  ## Screenshot placeholder

6. Grouping Data Using Multiple Columns (Task 6)
Grouping was used to summarize sales data based on more than one categorical variable.
Steps Followed:
1.	Selected multiple columns (e.g., Product, Region)
2.	Clicked Group By
3.	Switched to Advanced Mode
4.	Added multiple grouping columns
5.	Applied aggregation functions such as:
o	Sum of SalesAmount
o	Count of Transactions
Why Advanced Group By Was Used:
•	Allows grouping by more than one column
•	Enables multiple aggregations at once
•	Produces cleaner summary tables

 ## Screenshot placeholder
 
7. Final Transformation and Validation (Task 7)
After all transformations:
•	Data types were rechecked
•	Nulls and errors were reviewed
•	DataQualityFlag was validated
•	Aggregated results were verified for correctness
The dataset was confirmed to be:
•	Error-free
•	Consistent
•	Ready for modeling and visualization

 ## Screenshot placeholder
 
8. Loading Data into Power BI Model
Once transformations were complete, the data was loaded into the Power BI model.
This enabled:
•	Creation of measures
•	Building dashboards and reports
•	Confident analysis using clean data

 ## Screenshot placeholder
  
9. Conclusion
This lab demonstrated the importance of proper data preparation before analysis. By correcting data types, handling errors, introducing a DataQualityFlag, and grouping data using multiple columns, the dataset was transformed into a reliable and analysis-ready form.
The structured approach ensures reproducibility, transparency, and high data quality—critical components in real-world data analytics projects.

 ## Screenshot placeholder

10. Appendix 
Table showing the merge of stg_Sales and stg_products with Productname.

 ## Screenshot placeholder

Table showing the expanding of stg_products after choosing only Category and CostPrice.

  ## Screenshot placeholder

Table showing the expanding of stg_Regions after merging stg_Sales with stg_Regions under Country. Column 1 is the column for region.

 ## Screenshot placeholder
 
The calculations for a custom column show the number of sales made.

 ## Screenshot placeholder
 
The calculations for Profit using the values in the table.

 ## Screenshot placeholder
 
A custom column showing the range of total sales whether they are high, medium or low.

 ## Screenshot placeholder
 
A table showing the dimensions of the Products.
 
  ## Screenshot placeholder

Removing some columns from the dim_Products table.

  ## Screenshot placeholder

Creating the dim_Region table.

 ## Screenshot placeholder

 Creating a table showing the aggregate sales by each country.

 ## Screenshot placeholder
