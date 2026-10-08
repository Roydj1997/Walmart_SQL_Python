# Walmart Sales Analytics: SQL + Python

## Project Overview

**How can transactional sales data be transformed into actionable insights about revenue, product performance, customer behavior, and profitability?**

This project builds an end-to-end analytics workflow using **Python and PostgreSQL** to acquire, clean, transform, store, and analyze Walmart sales data.

The project combines **Python-based data preparation and feature engineering with PostgreSQL-based SQL analysis** to answer business-focused questions around sales performance, product categories, branches, payment methods, customer behavior, and profitability.

## Project Overview

![Project Pipeline](https://github.com/najirh/Walmart_SQL_Python/blob/main/walmart_project-piplelines.png)


Here, we utilize Python for data processing and analysis, SQL for advanced querying, and structured problem-solving techniques to solve key business questions. The project is ideal for data analysts looking to develop skills in data manipulation, SQL querying, and data pipeline creation.

---

## Project Steps

### 1. Set Up the Environment
   - **Tools Used**: Visual Studio Code (VS Code), Python, SQL (PostgreSQL)
   - **Goal**: Create a structured workspace within VS Code and organize project folders for smooth development and data handling.

### 2. Set Up Kaggle API
   - **API Setup**: Obtain your Kaggle API token from [Kaggle](https://www.kaggle.com/) by navigating to your profile settings and downloading the JSON file.
   - **Configure Kaggle**: 
      - Place the downloaded `kaggle.json` file in your local `.kaggle` folder.
      - Use the command `kaggle datasets download -d <dataset-path>` to pull datasets directly into your project.

### 3. Download Walmart Sales Data
   - **Data Source**: Use the Kaggle API to download the Walmart sales datasets from Kaggle.
   - **Dataset Link**: [Walmart Sales Dataset](https://www.kaggle.com/najir0123/walmart-10k-sales-datasets)
   - **Storage**: Save the data in the `data/` folder for easy reference and access.

   - ** Or download the CSV, unzip it in the project folder, and start the data wrangling.

### 4. Install Required Libraries and Load Data
   - **Libraries**: Install necessary Python libraries using:
     ```bash
     pip install pandas numpy sqlalchemy, psycopg2
     ```
   - **Loading Data**: Read the data into a Pandas DataFrame for initial analysis and transformations.

### 5. Explore the Data
   - **Goal**: Conduct an initial data exploration to understand data distribution, check column names, types, and identify potential issues.
   - **Analysis**: Use functions like `.info()`, `.describe()`, and `.head()` to get a quick overview of the data structure and statistics.

### 6. Data Cleaning
   - **Remove Duplicates**: Identify and remove duplicate entries to avoid skewed results.
   - **Handle Missing Values**: Drop rows or columns with missing values if they are insignificant; fill values where essential.
   - **Fix Data Types**: Ensure all columns have consistent data types (e.g., dates as `datetime`, prices as `float`).
   - **Currency Formatting**: Use `.replace()` to handle and format currency values for analysis.
   - **Validation**: Check for any remaining inconsistencies and verify the cleaned data.

### 7. Feature Engineering
   - **Create New Columns**: Calculate the `Total Amount` for each transaction by multiplying `unit_price` by `quantity` and adding this as a new column.
   - **Enhance Dataset**: Adding this calculated field will streamline further SQL analysis and aggregation tasks.

### 8. Load Data into PostgreSQL
   - **Set Up Connections**: Connect to PostgreSQL using `sqlalchemy` and load the cleaned data into each database.
   - **Table Creation**: Set up tables in PostgreSQL using Python SQLAlchemy to automate table creation and data insertion.
   - **Verification**: Run initial SQL queries to confirm that the data has been loaded accurately.

### 9. SQL Analysis: Complex Queries and Business Problem Solving
   - **Business Problem-Solving**: Write and execute complex SQL queries to answer critical business questions, such as:
     - Revenue trends across branches and categories.
     - Identifying best-selling product categories.
     - Sales performance by time, city, and payment method.
     - Analyzing peak sales periods and customer buying patterns.
     - Profit margin analysis by branch and category.
   - **Documentation**: Keep clear notes of each query's objective, approach, and results.

### 10. Project Publishing and Documentation
   - **Documentation**: Maintain well-structured documentation of the entire process in Markdown or a Jupyter Notebook.
   - **Project Publishing**: Publish the completed project on GitHub or any other version control platform, including:
     - The `README.md` file (this document).
     - Jupyter Notebooks (if applicable).
     - SQL query scripts.
     - Data files (if possible) or steps to access them.

---

## Requirements

- **Python 3.8+**
- **SQL Database**: PostgreSQL
- **Python Libraries**:
  - `pandas`, `numpy`, `sqlalchemy`, `mysql-connector-python`, `psycopg2`
- **Kaggle API Key** (for data downloading)
- ** Or download the CSV, unzip it in the project folder, and start the data wrangling.



## Business Questions

The analysis uses PostgreSQL to answer the following business-focused questions:

1. **Payment Method Analysis**
   - What are the different payment methods?
   - How many transactions and how many quantities were sold through each payment method?

2. **Highest-Rated Category by Branch**
   - Which category has the highest average rating in each branch?

3. **Busiest Day by Branch**
   - Which day of the week has the highest number of transactions for each branch?

4. **Quantity Sold by Payment Method**
   - What is the total quantity of items sold through each payment method?

5. **Category Ratings by City**
   - What are the minimum, maximum, and average ratings for each category in each city?

6. **Category Revenue & Profitability**
   - What is the total revenue and calculated profit for each category?

7. **Preferred Payment Method by Branch**
   - What is the most commonly used payment method in each branch?

8. **Sales by Time of Day**
   - How are transactions distributed across Morning, Afternoon, and Evening for each branch?

9. **Year-over-Year Revenue Decline**
   - Which five branches experienced the highest revenue decrease ratio when comparing 2023 revenue with 2022 revenue?
   - 


## Tech Stack

- **Programming:** Python
- **Data Manipulation:** Pandas, NumPy
- **Database:** PostgreSQL
- **SQL:** PostgreSQL / SQL
- **Database Connectivity:** SQLAlchemy, psycopg2
- **Data Source:** Kaggle API
- **Environment:** Jupyter Notebook


## Project Workflow

Kaggle Dataset
      ↓
Kaggle API
      ↓
Python / Pandas
      ↓
Data Cleaning & Validation
      ↓
Feature Engineering
      ↓
PostgreSQL
      ↓
SQL Business Analysis
      ↓
Business Insights

## Data Preparation & Feature Engineering

The raw Walmart sales dataset was prepared using Python before being loaded into PostgreSQL for analysis.

### Data Preparation

- Loaded the dataset using **Pandas**
- Inspected the dataset structure and data types
- Checked for missing values and duplicate records
- Converted columns to appropriate data types
- Standardized relevant fields for analysis
- Validated the cleaned dataset before database loading

### Feature Engineering

A new `Total` field was created to represent the total transaction value:

`Total = Unit Price × Quantity`

The cleaned and transformed dataset was then loaded into **PostgreSQL** using **SQLAlchemy** and `psycopg2` for further SQL-based analysis.


## Results and Insights

This section will include your analysis findings:
- **Sales Insights**: Key categories, branches with highest sales, and preferred payment methods.
- **Profitability**: Insights into the most profitable product categories and locations.
- **Customer Behavior**: Trends in ratings, payment preferences, and peak shopping hours.


