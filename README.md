# Accounts Payable Analytics Dashboard
Interactive AP dashboard designed using Microsoft Excel, Pivot tables, Pivot charts and slicers. This analyses invoice aging, vendor payment trends, invoice count and average overdue days based on vendor.
# Overview
## Business Problem
Accounts payable represents the money a business owes its vendors for goods and services bought on credit that have not yet been paid. Businesses often manage invoices from multiple vendors across different payment statuses and currencies. This makes accounts payable management a critical financial process. Organizations may face overdue payments, duplicate payments and limited visibility into outstanding liabilities without effective monitoring. This could negatively impact supplier relationships and cash flow management. Therefore, it is important to analyze accounts payable data for understanding the current financial position and supporting timely payment decision. 
## Business Goal
The objective is to analyze accounts payable performance through an interactive Microsoft Excel dashboard. This dashboard monitors vendor payment performance, invoice aging, outstanding balances, payment trends and currency exposure. It provides a clear overview of AP activity across vendors, years and payment statuses to finance teams to support faster, data driven financial decision making.
## About the Dataset
This project used synthetic Accounts Payable dataset for portfolio purposes from Kaggle. It includes 800 invoice records with 9 variables. The dataset reflects vendor details, invoice and payment details. The following image shows all the variables in this dataset.
<img width="147" height="285" alt="image" src="https://github.com/user-attachments/assets/0fbbb7b8-2388-402a-ac34-b4101c2d13d1" />
# Dashboard Preview
## Dashboard 1 – Financial Overview
 <img width="975" height="665" alt="image" src="https://github.com/user-attachments/assets/3980c3df-bb4e-45ae-9554-9893cffaf4ff" />
## Dashboard 2 – Payment Performance
 <img width="975" height="729" alt="image" src="https://github.com/user-attachments/assets/3d93c06d-e194-4901-b7a5-5737b2ff1207" />

# Tools Used
•	Microsoft Excel
•	Pivot Tables
•	Pivot Charts
•	Slicers
•	Excel Formulas – KPI Calculations, IF, IFS, XLOOKUP formulas, Date functions, Currency Conversion

# Data Preparations
Parameters	Observations
Number of observations	800
Number of variables	9
Currencies	GBP, USD, CAD, AUD, EUR
Reporting Currency	USD
Date Range	2023-2025

•	Imported Accounts Payable dataset into Microsoft Excel for analysis.
•	Validated data quality by checking duplicate records. No duplicate invoices were identified.
•	Checked missing values and identified blanks in the PaidDate column. These were retained because unpaid (partial and open) invoices do not have a paid date. 
•	Converted multiple currencies into USD using the Microsoft 365 Currency data type and an XLOOKUP formula.
•	Calculated outstanding amount for unpaid invoices. Partial payment invoices were assigned to N/A because the dataset does not contain the sufficient information to calculate the remaining balance accurately.
•	Calculated overdue days by subtracting each invoice’s due date from a reporting reference date (30/07/2025). The reference date was dynamically generated using invoice date and due date.
•	Created aging bucket based on the overdue days to classify outstanding invoices into Current, 1–30 Days, 31–60 Days, 61–90 Days and 90+ Days categories.
•	Created KPI calculations including Total Payable Amount, Total Outstanding Amount, Days Payable Outstanding (DPO), Outstanding Rate, and Open Invoice Rate for dashboard reporting.

# Key Business Questions and Insights
Q1 – Which vendors have the highest accounts payable exposure based on invoice value, payments made and outstanding balances?
1.	BluePrints has the highest total invoice amount, indicating it represents the largest supplier in the dataset.
2.	ABC Supplies has the highest outstanding amount approximately 152K. This suggests that it has the largest unpaid liability among all the vendors, while Fast travel has the lowest outstanding balance, indicating lower unpaid exposure than the other vendors.
3.	 All five vendors show a clear gap between invoice amounts and paid amount. This highlights the remaining outstanding obligations that require ongoing accounts payable monitoring.
Q2 – How have invoice amounts, payments and outstanding liabilities changed across reporting years (2023–2025)?
1.	Total invoice amount declined from 2023 to 2025, indicating a reduction in overall supplier invoice volume during the reporting period.
2.	2024 recorded the highest outstanding amount.
3.	Outstanding liabilities decreased significantly in 2025. This indicates that lower remaining payable balance compared with previous years.
4.	Total paid amount is also declined over the 3-year period, lower payment activity alongside the reduction in invoice volume.
Q3 – Which vendors have the highest number of overdue outstanding invoices across different aging categories?
1.	BluePrints has the highest number of invoices in the 90+ days aging bucket. This indicates the highest concentration of long overdue outstanding invoices among all vendors.
2.	The majority of outstanding invoices fall within the 90+ day aging bucket.
3.	Almost every vendor has nearly 100 invoices that overdue by more than 90 days which highlights the significant payment risk across multiple vendors.
Q4 – Which currencies have the highest invoice value and outstanding payable exposure after after USD conversion?
1.	GBP has the highest total invoice amount, making it the largest supplier payment exposure among all currencies.
2.	GBP also has the greatest outstanding balance and indicates the highest unpaid liability after currency conversion.
3.	AUD and CAD have the lowest outstanding balances, suggesting comparatively lower unpaid exposure in these currencies.
Q5 - Which vendors have the longest average overdue payment period and therefore represent the highest overdue payment risk?
1.	ABC Supplies has the highest average overdue period. This shows the greatest overdue payment risk among all the vendors.
2.	All vendors have an average overdue period exceeding 280 days, which highlights a large backlog of long overdue outstanding invoices in the reporting period.
Q6 – How has the distribution of open, paid and partial invoices changed across invoice years?
1.	2024 recorded the highest number of open invoices. This indicates the largest number of unpaid invoices during this period.
2.	Paid invoices were highest in 2023, suggesting stronger payment completion compared with other years.
3.	Partial invoices remained consistently high in 2023 and 2024. This shows a significant number of invoices were partially settled.
Q7 – How do monthly invoice amounts compare with supplier payments over time?
1.	Monthly invoice amounts consistently remains higher than monthly payment amounts throughout the reporting periods. This highlights the ongoing accounts payable obligations each month. 
2.	Payment activity is more stable than invoice activity as most monthly payments remaining below 40K.
3.	The gap between invoice amounts and payments varies by month, highlighting months where outstanding liabilities may accumulate due to lower payment activity relative to invoice volume.

# Skills Demonstrated
	Data cleaning
	Excel Dashboard Design
	Pivot Tables
	Pivot Charts
	KPI Development
	Currency Conversion
	Financial Reporting
	Data Visualization

