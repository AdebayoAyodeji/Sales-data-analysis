## Online Retail sales Analysis

### Project Overview

This project is aimed at providing insights into the sales of a growing online retail store, looking to identify revenue drivers and performance trends from both operational and marketing perspectives.

## Business Objectives:

Business leaders wants to know what the major contributing factors are to the revenue, viewing the metrics from both an operations and marketing perspective, so they can strategically plan for next year.

## Defined Metrics:

- Region is generating the highest and the lowest revenue. The CEO of the retail store is interested to view revenue data for the year 2011 only. 
- Top 10 countries which are generating the highest revenue and the quantity sold along with the revenue generated excluding United Kingdom.
- Top 10 customers by revenue.
- The CEO is looking to gain insights on the demand for their products. He wants to look at all countries and see which regions have the greatest demand for their products
 excluding the United Kingdom. He's more interested in viewing the countries that have expansion opportunities.

## Data Source

The dataset is online retail data in CSV 
[Download dataset here](https://onedrive.live.com/personal/015f7f966231f634/_layouts/15/doc.aspx?resid=15F7F966231F634!s4120b27c2be34c68a737f964921c6d6b&cid=015f7f966231f634)

![Online Retail Data Set  - Excel Image](https://github.com/user-attachments/assets/dc8917b3-5e62-4d8d-b74e-963ab625a38c)

## Tools
The tools used for this projects are;

- Power Query - I explored the data using Power Query (Identified missing values, inconsistent formats, or outliers).
- Power BI - Created insightful visuals.

## Data Cleaning 
The data was loaded into Power BI. leveraged the transform techniques through Power Query to organise, handled missing values and created some useful columns needed for my analysis. I observed that the data contains some returns to the store which are provided in negative quantities and there are unit prices which were input in error.
The methods and formulars used for cleaning; 

- IN POWER Query

TO DELETE UNWANTED NUMBERS;

Filtered quantity column > NUMBER FILTER > GREATER OR EQUAL TO 1 (to hide negative numbers)
Filtered Price column > NUMBER FILTER > GREATER OR EQUAL TO 0 (to hide negative numbers)

I deleted some unspecified location in the country region.
I deleted blanks in the customer ID column to ensure data accuracy and to prevent our result from been skewed.

- IN POWER BI;

I could have used the drill function on the invoicedate but I wanted to create columns for the month and year. So, I extracted both from the Invoicedate column in Power BI using DAX: 

MonthNumber = MONTH('Table'[Date])
MonthName = FORMAT('Table'[Date], "MMM")
Year = Year ('Table'[Date], "MMM")

Created a revenue column;
 	Revenue = ('Online Retail'[Quantity]) * ('Online Retail'[Unit Price])

Below is the data after cleaning;
  ![Power BI Desktop Image](https://github.com/user-attachments/assets/5c51800e-76c4-41f3-b80d-9907ca77e6ba)

## Result
After the cleaning and data manipulation process. I came up with visuals to clearly answer the business questions;


