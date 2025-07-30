# Walmart Data Analysis : using SQL and Python 

## Project Overview

This project is a complete end-to-end data analysis workflow focused on uncovering valuable business insights from Walmart's sales data. Using Python, the data is cleaned, transformed, and prepared before being loaded into a relational database. SQL is then used to perform complex queries and answer important business questions. This project is a great hands-on exercise for anyone looking to build practical skills in data analysis, SQL, and working with real-world datasets.

---

## Project Steps

### 1. Set Up the Environment
   - **Tools I Used** : Visual Studio Code (VS Code), Python, and MySQL
   - **Purpose** : To create a clean and organized workspace in VS Code by setting up project folders and preparing the environment for writing code, managing data, and 
                  running SQL queries smoothly.

### 2. Set Up Kaggle API
   - **API Setup** : I generated my Kaggle API token by going to my Kaggle account settings and downloading the kaggle.json file.
   - **Configure Kaggle** : 
      - Created a .kaggle folder in my user directory
      - Moved the kaggle.json file into that folder.
      - Used the following command to download the dataset directly into the project :
        `` kaggle datasets download -d najir0123/walmart-10k-sales-datasets ``

### 3. Download Walmart Sales Data
   - **Data Source** : I used the Kaggle API to download the Walmart sales dataset directly from Kaggle.
   - **Dataset Link** : [Walmart Sales Dataset](https://www.kaggle.com/najir0123/walmart-10k-sales-datasets)
   - **Storage**: After downloading, I saved the dataset inside the data/ folder to keep everything organized and easy to access during analysis.

### 4. Install Required Libraries and Load Data
   - **Libraries** : I installed the necessary Python libraries using the following command :  
                     `` pip install pandas numpy sqlalchemy mysql-connector-python ``
   - **Loading Data** : After setting up the environment, I loaded the dataset into a Pandas DataFrame to begin cleaning, exploring, and analyzing the sales data.

### 5. Explore the Data
   - **Purpose** : I started with a quick exploration of the dataset to understand the structure, column names, data types, and spot any missing or unusual values.
   - **Initial Analysis** : Used basic Pandas functions like .head(), .info(), and .describe() to get a summary of the data and its distribution.

### 6. Data Cleaning
   - **Duplicate Removal** :  I removed any duplicate records to keep the analysis accurate.
   - **Missing Values** : Handled missing data by either dropping irrelevant rows or filling values where needed.
   - **Fix Data Types** :  Converted columns to the correct data types — for example, dates to datetime and prices to float.
   - **Currency Formatting** : Used .replace() to clean and convert currency values into a usable numeric format.
   - **Final Validation** : Checked the cleaned dataset for consistency and confirmed it's ready for analysis.

### 7. Feature Engineering
   - **New Column Creation** : I added a Total Amount column by multipling unit_price with quantity for each transaction.
   - **Why This Helps** : Including this calculated field made it easier to perform SQL aggregations and analyze total sales in later steps.
     
### 8. Load Data into MySQL 
   - **Database Connection** : I connected to MySQL using SQLAlchemy and established the connection through Python.
   - **Table Setup** : Used Python code to create tables and insert the cleaned DataFrame directly into the MySQL database.
   - **Data Check** : Ran a few basic SQL queries to make sure the data was loaded correctly and matched the original DataFrame.

### 9. SQL Analysis : Complex Queries and Business Problem Solving
   - **Objective** : I wrote and executed complex SQL queries to answer key business questions using the cleaned Walmart sales data.
   - **Key Analyses Included** :
     - Revenue trends across different branches and product categories
     - Identified best-selling product categories.
     - Sales performance by time, city and payment method.
     - Analyzed peak sales periods and customer buying patterns.
     - Profit margin analysis by branch and category.
   - **Documentation** : For each query, I documented the goal, logic, and key insights to ensure clarity and reproducibility.
     
### 10. Project Publishing and Documentation
   - **Documentation** : I documented the full project workflow using Markdown and Jupyter Notebooks to make the process easy to follow and understand.
   - **Project Publishing** : The project is published on GitHub and includes:
     - A well-structured README.md with project details, setup steps, and usage instructions.
     - Python scripts and/or Jupyter Notebooks used for data cleaning, transformation, and analysis.
     - SQL scripts for business-related queries and analysis.
     - Either the dataset itself or clear instructions on how to access/download it (e.g., from Kaggle).

---

## Requirements

- **Python 3.8+**
- **SQL Database** : MySQL
- **Python Libraries** :
  - `pandas`, `sqlalchemy`, `mysql-connector-python`
- **Kaggle API Key** : Required for downloading the dataset.

## Getting Started

1. Clone the repository :
   git clone <repo-url>
   
2. Install Python libraries :
   pip install -r requirements.txt
   
4. Set up your Kaggle API, download the data, and follow the steps to load and analyze.

---

## Project Structure

```plaintext
|-- data/                     # Contains raw and cleaned datasets
|-- sql_queries/              # SQL scripts for analysis and queries
|-- notebooks/                # Jupyter notebooks for Python analysis
|-- README.md                 # Project overview and setup guide
|-- requirements.txt          # List of required Python libraries
|-- main.py                   # Script for processing and loading data

```
---

## Results and Insights

Here are some key takeaways from the analysis performed on the Walmart sales data:

- **Sales Insights** : Identified top-performing product categories, branches with the highest sales, and commonly used payment methods.
- **Profitability** : Analyzed which product categories and locations generated the most profit.
- **Customer Behavior** : Observed trends in customer ratings, preferred payment types, and peak shopping hours.

## Future Enhancements

Some improvements and extensions I plan to explore in the future:

- **Dashboard Integration** : Connect the project with Power BI or Tableau to create interactive dashboards for better visualization and reporting.
- **More Data Sources** : Combine additional datasets to gain deeper insights and expand the scope of analysis.
- **Pipeline Automation** : Automate the data pipeline to handle real-time data ingestion, cleaning, and analysis more efficiently.

---

## License

This project is licensed under the MIT License. 

---

## Acknowledgments

- **Data Source** : Kaggle’s Walmart Sales Dataset
- **Inspiration** : Walmart’s business case studies on sales and supply chain optimization. 

---
