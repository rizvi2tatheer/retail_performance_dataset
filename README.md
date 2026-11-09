# Retail Performance Analysis

## Project Overview

This project focuses on analyzing customer shopping behavior using Python, MySQL, and Power BI. The objective is to explore customer purchasing patterns, identify meaningful trends, clean and transform raw data, and present key business insights through an interactive Power BI dashboard.

The project follows an end-to-end data analytics workflow, starting with data exploration and cleaning in Python, followed by database integration and interactive visualization in Power BI.

## Project Objectives

- Perform Exploratory Data Analysis (EDA) to understand the dataset.
- Identify and handle missing values and inconsistencies.
- Clean and standardize dataset columns.
- Perform feature engineering to create meaningful customer segments.
- Analyze customer purchasing patterns and preferences.
- Prepare the cleaned dataset for MySQL database integration.
- Build an interactive Power BI dashboard to visualize key business metrics.

## Dataset Description

The dataset contains **3,900 records and 18 columns**, representing customer shopping transactions and purchasing behavior.

### Key Features

| Column | Description |
|---|---|
| Customer ID | Unique customer identifier |
| Age | Age of the customer |
| Gender | Customer gender |
| Item Purchased | Product purchased |
| Category | Product category |
| Purchase Amount (USD) | Amount spent on the purchase |
| Location | Customer location |
| Size | Purchased product size |
| Color | Product color |
| Season | Season associated with the purchase |
| Review Rating | Customer review rating |
| Subscription Status | Customer subscription information |
| Shipping Type | Shipping method selected |
| Discount Applied | Whether a discount was applied |
| Promo Code Used | Whether a promo code was used |
| Previous Purchases | Number of previous purchases |
| Payment Method | Payment method used |
| Frequency of Purchases | How frequently the customer shops |

## Tools & Technologies

- **Python** – Data analysis and manipulation
- **Pandas** – Data cleaning and transformation
- **Jupyter Notebook** – Analysis environment
- **MySQL** – Database management
- **SQLAlchemy & PyMySQL** – Database connectivity
- **Power BI** – Interactive dashboard and visualization

## Project Workflow

### 1. Data Loading and Exploration (Python)

- Imported the dataset using Pandas.
- Examined the dataset structure, dimensions, and data types.
- Used descriptive statistics to understand numerical variables.
- Identified missing values and examined categorical distributions.

### 2. Data Cleaning and Preprocessing

- Identified missing values in the `Review Rating` column.
- Found 37 missing values in the initial dataset.
- Handled missing ratings using the median review rating of the corresponding product category.
- Verified the dataset after handling missing values.
- Standardized column names by converting them to lowercase and replacing spaces with underscores.
- Renamed columns for better readability and consistency.

### 3. Feature Engineering

Created additional features to support customer segmentation and behavioral analysis.

**Age Group Segmentation**

Used Pandas `qcut()` to divide customers into four age groups:

- Young
- Young Adult
- Middle-Age
- Senior

**Purchase Frequency Conversion**

Converted categorical purchase frequency values into approximate numerical day intervals.

| Purchase Frequency | Days |
|---|---:|
| Weekly | 7 |
| Fortnightly / Bi-Weekly | 14 |
| Monthly | 30 |
| Quarterly / Every 3 Months | 90 |
| Annually | 365 |

### 4. Data Redundancy Check

- Compared the `discount_applied` and `promo_code_used` columns.
- Found that both columns contained identical values across all records.
- Identified `promo_code_used` as a potentially redundant column and demonstrated its removal.

### 5. MySQL Database Integration

Prepared the cleaned dataset for database storage using:

- SQLAlchemy
- PyMySQL
- MySQL

The notebook includes a database connection workflow to load the transformed data into a MySQL database.

**Database:** `retail_dataset`  
**Table:** `customer_data`

### 6. Power BI Dashboard

Developed an interactive dashboard to explore customer shopping behavior and purchasing patterns.

**Key Performance Indicators (KPIs):**
- Total Customers
- Average Purchase Amount
- Average Review Rating

**Dashboard Visualizations:**
- Revenue by Category
- Sales by Category
- Percentage of Customers by Subscription Status
- Revenue by Age Group
- Sales by Age Group

**Interactive Filters:**
- Subscription Status
- Gender
- Category
- Shipping Type

These filters allow users to explore different customer segments and compare purchasing patterns across categories.

## Key Observations

Based on the exploratory analysis performed in Python:

- The dataset contains 3,900 customer purchase records.
- Clothing is the most frequently occurring product category.
- Male customers represent the largest gender group in the dataset.
- Non-subscribers form the majority of the recorded customer entries.
- Spring has the highest number of purchase records among the seasons.
- The `Review Rating` column was the only column containing missing values in the initial dataset.
- The discount and promo-code columns contain identical values in the available records.

## Repository Structure

```text
Customer-Shopping-Behavior-Analysis/
│
├── README.md
│
├── Untitled1.ipynb
│
├── Retail_business_dashboard.pbix
│
└── customer_shopping_behavior.csv

## Project Outcome

This project demonstrates an end-to-end data analytics workflow involving data exploration, data cleaning, feature engineering, database integration, and business intelligence reporting.

It highlights how raw customer shopping data can be transformed into a structured dataset and presented through an interactive dashboard to support better understanding of customer behavior and purchasing patterns.

## Future Improvements

- Perform deeper customer segmentation.
- Analyze customer retention and repeat purchasing behavior.
- Explore relationships between discounts, subscriptions, and purchase amounts.
- Add more advanced SQL-based business analysis.
- Enhance the Power BI dashboard with additional KPIs and drill-through functionality.

---

**Project Focus:** Data Analytics | Exploratory Data Analysis | Data Cleaning | Python | MySQL | Power BI
