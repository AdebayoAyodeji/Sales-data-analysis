## Online Retail sales Analysis

### Project Overview

This project aims to provide insights into the sales performance of a growing online retail store by identifying revenue drivers and performance trends from both operational and marketing perspectives, enabling business leaders to plan strategically for the year ahead.

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
After the cleaning and data manipulation process. I came up with visuals to clearly answer the business questions Using Power BI.

- Monthly Revenue Trend - 2011
![Monthly Revenue Trend](https://github.com/user-attachments/assets/61ce75fe-9d5f-4848-b87f-348a76e6dee4)

- Top 10 Customers By Revenue
![Top 10 customers by revenue](https://github.com/user-attachments/assets/48cf3e85-f75f-45aa-87ea-dcfec86426a4)

- Top 10 Revenue-Generating Countries
![top 10 country by revenue ](https://github.com/user-attachments/assets/7dffcc2b-4c1d-4afd-819f-e7478214135b)

- Product Demand By Region
![Product demand by country](https://github.com/user-attachments/assets/f7e24d06-bb20-47e0-96b5-f8d016178548)

- Total Revenue Generated
![Total Revenue ](https://github.com/user-attachments/assets/b83258cd-23a8-4e15-80d2-fbd638cef88f)

1. Revenue trends show low sales in Q1 & Q2, a spike from September to November, then a drop in December. However, a decline is observed in December.
2. Germany led with $81B in revenue and the highest quantity sold, followed by France and EIRE, while Australia, Sweden, and Japan generated the least revenue.
3. Customer 14646 is the top revenue-generating customer, contributing $280,206.02, followed by Customer 14911 with $143,825.06. The lowest contributors are Customers 13263
   and 14606
5. European countries appeared to be the most dominating region in terms of product demand.

## Recommendations:

- Consider expanding product offerings for the next festive season and introduce seasonal discounts to boost sales. A targeted market survey in low-revenue months would
  identify products that better meet customer needs.

- Focus on offering targeted discounts and quality products that match high-value customers’ preferences. Refine product strategies based on regional demand to boost sales
  in underperforming markets and enhance overall performance.

  ## Reference;
Stack overflow

r/datascience. Reddit

  
  






