# Sales-Insights-using-PowerBI

## Overview

AtliQ Hardware is a company based in India that supplies computer hardware and peripherals across the country. The business faces challenges in tracking and analyzing sales data from various regional offices. The sales director requires an efficient and reliable way to understand company sales and make informed decisions.

In this project, I simulated a solution to help AtliQ Hardware solve their sales tracking and reporting issues. The solution involves building an interactive and informative sales dashboard using MySQL, Power BI, and ETL processes.

## Business Problem

AtliQ Hardware’s sales director is struggling with:
- Tracking sales across regional offices.
- Handling large amounts of data from regional managers.
- Analyzing sales performance effectively and making data-driven decisions.

The sales director needs an easy-to-use dashboard to understand sales trends, revenue, and top-performing products and customers.

## Solution

The solution is to build a dashboard that provides insights into the company’s sales data, showing key metrics such as:
- Total revenue
- Sales quantity by product and customer
- Sales trends
- Regional sales performance

This dashboard is built using:
- **MySQL** for data exploration and extraction.
- **Power BI** for data transformation (ETL process) and visualization.

---

## Project Structure

This repository contains the following components:
- **Data Exploration**: SQL queries used to extract relevant data from the MySQL database.
- **ETL Process**: Power BI file that contains data transformations and visualizations.
- **Dashboard**: A Power BI dashboard showing key sales insights.

### Data Exploration (SQL Queries)

The data is stored in 5 tables in the MySQL database:
- **customers**: Information about the customers.
- **date**: Date information.
- **markets**: Regional market data.
- **products**: Product details.
- **transactions**: Sales transactions.

Key observations:
- There are 17 markets, 279 products, and 38 customers.
- The data spans from January 2018 to June 2020.
- A significant drop in revenue in 2020, down 42% compared to 2019.
- Some transactions are in USD (to be normalized to INR).

### ETL Process

The ETL process in Power BI involves:
- **Extracting** the data from MySQL.
- **Transforming** the data by cleaning, filtering, and adding necessary calculations.
- **Loading** the cleaned data into Power BI for visualizations.

### Data Modeling

In Power BI, I connected five tables:
- **Sales Transactions**: Main table for transactions.
- **Sales Customers**: Linked via `customer_code`.
- **Sales Date**: Linked via `date`.
- **Sales Products**: Linked via `product_code`.
- **Sales Markets**: Linked via `market_code`.

### Measures Created

- **Revenue**: Sum of the revenue column.
- **Sales Quantity**: Sum of the sales quantity column.

### Data Cleaning

- Removed invalid sales amounts (0 and -1 values).
- Filtered out non-Indian markets (Paris and New York).
- Normalized USD to INR in the sales transactions using a conditional formula.
- Removed duplicate values.

---

## Dashboard Insights

The dashboard presents the following key metrics:
- **Total Revenue** and **Sales Quantity** over the period.
- **Revenue and Sales by Market** to show regional performance.
- **Revenue Trend** to analyze how sales are progressing over time.
- **Top 5 Customers** and **Top 5 Products** to identify key drivers of sales.

The dashboard can be filtered by **Year** and **Month** to provide granular insights.

---

## Technical Procedures

1. **MySQL Database**:
   - Ensure you have MySQL installed.
   - Load the database schema and data into MySQL Workbench.
   - Run the provided SQL queries to explore and understand the data.

2. **Power BI**:
   - Open the provided Power BI file.
   - Connect to the MySQL database and load the data.
   - Apply the transformations as described in the ETL process.

3. **Dashboard**:
   - After the transformations, the dashboard will automatically update with key metrics.
   - Use the filters to explore the data interactively.

---

## Technologies Used

- **MySQL**: For data storage and querying.
- **Power BI**: For ETL process and visualizations.
- **SQL**: For data extraction and transformation.

