# Trigon_Corporation_Data_Forcasting
Create a report for Trigon that analyses their data for the year 2016 and predicts their 2017 sales strategy.

- we created a report to forcast Trigon Corporation's profit increase percentage, representative performance, warehouse purchase and product sales for 2016 fiscal year.

## Company AS IS:
1. Stored data in QuickBooks desktop version
2. No IT team

- We extracted data from QuickBooks and imported to MS Excel.
- The data tools we used were MS SQL Server, MS Excel, Tableau 10.1, IBM Watson

## Original Data Description:
- Many itemsdid not have an item number plus several line items did not have zip codes.
- Many superfluous details like research and development, early discount programs, samples, etc. were associated in the line item.
- Items not stored in inventory did not have an item number, special order items were not included in inventory and not billed as invoice.
- Country details were missing for most of the products.
- Item numbers were alphanumeric hence it was difficult to parse them.

## Data Cleansing Soutions
- Removed services that were listed as line items and assigned unique identifiers to all items.
- Included/ added countrry details and added missing zip codes.
- Columns for new data set: 
OrderID (Datatype should be integer not alphanumeric), Date, ItemID (Datatype should be integer not alphanumeric), Customer Name, Representative ID/ Name, Quantity, Price, Amount (Quantity * Price), Zip Code, Country
- Columns to eliminate from original data set:
Type (Unnecessary)
Memo (Unnecessary)
Num (Rename to Item ID)
Name ( Rename to Customer Name)
Balance (Unnecessary)
- Rows to eliminate from original data set:
Freight, EREF, Credit or No Charge Adj, Personal, Misc, SledgeHammer

## Data Report

- After cleaning the final data set we created an SSAS package on SQL Server and connected that to Tableau 10.1 cloud to create visualized data.

- Trigon Data Dashboard

![dashboard](https://cloud.githubusercontent.com/assets/24817774/22901795/da324884-f200-11e6-8cf2-f7d69842654b.PNG)

- Total sales made monthly and yearly for the year 2016.

![total_sales_monthly_quarterly](https://cloud.githubusercontent.com/assets/24817774/22900721/5b751484-f1fd-11e6-890d-90a4f5d25090.PNG)

- Total sales done by the sales representatives.

![sales_rep_total_sales](https://cloud.githubusercontent.com/assets/24817774/22901312/35655f40-f1ff-11e6-93eb-8e19cfe14a9f.PNG)

- Trigon Corporation's most frequent patronisers.

![most_frequent_patronisers](https://cloud.githubusercontent.com/assets/24817774/22901473/db462584-f1ff-11e6-9e73-df2e7cfaeec1.PNG)

- Products sold based on region

![products_sold_based_on_region](https://cloud.githubusercontent.com/assets/24817774/22901733/9edc4294-f200-11e6-9217-788bcb02bba5.PNG)

- Most products sold in 2016 

![most_sold_products](https://cloud.githubusercontent.com/assets/24817774/22901815/f7440a02-f200-11e6-8bee-6087d49b0ec9.PNG)

- 


