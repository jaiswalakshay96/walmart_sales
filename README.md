# Walmart - Store Sales Analysis

## About

This project's objectives are to study how sales strategies can be improved and optimized by analyzing sales data from Walmart. The dataset was obtained from the [Kaggle Walmart Sales Forecasting Competition](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting). Job seekers are given historical sales data for 45 Walmart stores located in various regions. Each store has many departments, and participants must project the sales for each department in each store. To add to the challenge, certain holiday markdown events are included in the dataset. These markdowns are known to affect sales, but it's challenging. [source] [https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting]

## Goals Of The Project

The main goal of this project is to obtain insight into Walmart's sales data in order to comprehend the various elements that influence sales at various branches.

## Concerning Data

The Walmart Sales Forecasting Competition on Kaggle (https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting) is where the dataset was found. The sales transactions from three separate Walmart branches—one each in Mandalay, Yangon, and Naypyitaw—are included in this dataset. There are 1000 rows and 17 columns in the data:

### Data Columns

| Column                  | Datatype       |
|-------------------------|----------------|
| Invoice_ID              | varchar(30) PK |
| Branch                  | varchar(5)     |
| City                    | varchar(30)    |
| Customer_type           | varchar(30)    |
| Gender                  | varchar(30)    |
| Product_line            | varchar(30)    |
| Unit_price              | decimal(10,2)  |
| Quantity                | double         |
| Tax_5_percent           | double         |
| Total                   | double         |
| Date                    | date           |
| Time                    | time           |
| Payment                 | varchar(20)    |
| Cogs                    | double         |
| Gross_margin_percentage | double         |
| Gross_income            | double         |
| Rating                  | double         |

## List of Analysis

### 1. Evaluation of Products

Analyze the data to identify the various product lines, the best-performing product lines, and the product lines that require improvement.

### 2. Analysis of Sales

The goal of this investigation is to provide an answer to the query about product sales trends. The outcome of this can assist us in gauging the success of every sales technique the company employs and the adjustments required to increase sales.

### 3. Analysis of Customers

The many customer segments, purchasing patterns, and profitability of each customer category are the focus of this investigation.

## Methodology Employed

1. **Data Wrangling:** In this initial stage, data is inspected to ensure that **NULL** and missing values are found, and data replacement techniques are applied to replace any missing or **NULL** values.

    - Construct a database.
    - Make a table and add data.
    - Choose which columns have null values. Since we specified **NOT NULL** for every column when constructing the tables, null entries are filtered out and there are no null values in our database.

2. **The process of feature engineering:** With this, we can create some new columns out of the ones that already exist.

    - Include a new column called `time_of_day` to provide information on sales in the morning, afternoon, and evening. This will assist in addressing the query of what time of day the majority of sales occur.
    - Include the extracted days of the week (Mon, Tue, Wed, Thur, Fri) on which the specified transaction occurred in a new column called `day_name`. This will provide some insight into the busiest week of the day for each branch.
    - Create a new column called `month_name` with the extracted months (Jan, Feb, Mar) of the year that the supplied transaction occurred. Assist in identifying the month with the most profit and sales for the year.

3. **Data Analysis for Exploration (EDA):** To address the stated concerns and objectives of this project, exploratory data analysis is carried out.
