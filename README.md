
🚗 Car Sales Analysis Dashboard – Power BI
🔹 Project Overview

The Car Sales Analysis Dashboard is an interactive Power BI project designed to analyze and visualize car sales performance across different regions, time periods, and product attributes.
This dashboard enables stakeholders to monitor key sales metrics, identify trends, and make data-driven business decisions.

🎯 Business Objective

The objective of this project is to design and develop a dynamic and interactive Car Sales Dashboard using Power BI.
The dashboard visualizes critical KPIs related to car sales, helping the business understand sales performance over time, track growth, and identify opportunities for improvement.

🛠 Tools & Technologies

Microsoft Power BI Desktop

Microsoft Excel (Data Source)

DAX (Data Analysis Expressions)

Date Table (Custom Calendar Table)

📂 Dataset Description

| Column Name   | Description                 |
| ------------- | --------------------------- |
| Car Model     | Model of the car            |
| Body Style    | Sedan, SUV, Hatchback, etc. |
| Color         | Car color                   |
| Sales Amount  | Total sales value           |
| Dealer Region | Sales region                |
| Company       | Manufacturer / Brand        |
| Date          | Transaction date            |
| Quantity      | Cars sold                   |

A separate Date Table was created to support:

Time intelligence functions

YTD, MTD, YOY calculations

📌 Problem Statement 1 – KPI Requirements
1. Sales Overview

Year-to-Date (YTD) Total Sales

Month-to-Date (MTD) Total Sales

Year-over-Year (YOY) Growth in Total Sales

Difference between YTD Sales and Previous YTD (PTYD) Sales

2. Average Price Analysis

YTD Average Price

MTD Average Price

YOY Growth in Average Price

Difference between YTD Avg Price and PTYD Avg Price

3. Cars Sold Metrics

YTD Cars Sold

MTD Cars Sold

YOY Growth in Cars Sold

Difference between YTD Cars Sold and PTYD Cars Sold

📊 Problem Statement 2 – Visualizations

The dashboard includes the following visuals:

YTD Sales Weekly Trend

Line chart showing weekly YTD sales trend

YTD Total Sales by Body Style

Pie chart for body style contribution

YTD Total Sales by Color

Pie chart for color-wise sales

YTD Cars Sold by Dealer Region

Map chart showing geographical sales distribution

Company-Wise Sales Trend (Grid)

Table showing company and YTD sales

Detailed Sales Grid

Complete transactional details for all car sales

🔐 Row-Level Security (RLS)

Row-Level Security is implemented based on Dealer Region.

Users can only view data for their assigned region

Ensures data privacy and secure access

Real-time dynamic filtering at user level

🧠 Key DAX Measures Used
YTD Sales = 
TOTALYTD(SUM(Sales[Sales Amount]), 'Date'[Date])

MTD Sales = 
TOTALMTD(SUM(Sales[Sales Amount]), 'Date'[Date])

PTYD Sales = 
CALCULATE(
    [YTD Sales],
    SAMEPERIODLASTYEAR('Date'[Date])
)

YOY Sales Growth % = 
DIVIDE([YTD Sales] - [PTYD Sales], [PTYD Sales], 0)

YTD Cars Sold = 
TOTALYTD(SUM(Sales[Quantity]), 'Date'[Date])

📈 Key Business Insights

Identified top-performing regions by total sales

Analyzed seasonal trends using weekly YTD sales

Found body styles contributing most to revenue

Discovered high average price segments

Enabled region managers to access only their data using RLS

🚀 How to Use the Dashboard

Download the .pbix file

Open in Power BI Desktop

Refresh Excel data source

Use slicers (Date, Region, Body Style)

Explore KPIs and visual insights

📎 Project Files

Car_Sales_Analysis.pbix

car_sales_data.xlsx

Date_Table.xlsx

README.md

🔮 Future Enhancements

Integrate SQL or API data source

Add drill-through reports

Publish to Power BI Service

Implement incremental refresh

👤 Author

Name: Ayyanar M

Role: Power BI Developer

Skills: Power BI, DAX, Excel, SQL, Data Visualization

⭐ Conclusion

The Car Sales Analysis Dashboard provides a complete view of sales performance with real-time KPIs, advanced time intelligence, and secure access using RLS.
This project demonstrates strong hands-on skills in Power BI, business analytics, and dashboard design

The dataset contains detailed information about car sales transactions.
