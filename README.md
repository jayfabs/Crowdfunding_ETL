# Crowdfunding ETL

This project is focused on extracting, transforming, and loading data from a crowdfunding dataset into a Postgres database. The main goal is to create four tables from the raw data: Campaign, Category, Subcategory, and Contacts.

## Tools used

Python
Pandas library
Postgres
Data Cleaning Process

## The data cleaning process involved the following steps:

Read in the CSV file using the pandas library.
Split the Category and Subcategory column into two separate columns.
Create separate tables for Category and Subcategory with specified ID columns.
Edit the Campaign table by dropping unnecessary columns and ensuring correct data types.
Merge the Category ID and Subcategory ID columns into the Campaign table.
Read in the Contacts JSON file.
Use a for loop to separate each row into columns by the "," delimiter, creating the Contacts dataframe with four columns.
Use SQL to create each table in Postgres, ensuring proper primary key and foreign key labels.
Import the CSV file containing the data frames in the specific order: Category, Subcategory, Contacts, and Campaign (last).

## Files included

Crowdfunding_ETL.ipynb: Jupyter notebook containing the Python code for ETL process.
Crowdfunding_ETL.sql: SQL file containing the code for creating tables in Postgres.

## Usage

Clone the repository to your local machine.
Create a new Postgres database.
Update the connection string in the Jupyter notebook.
Run the Jupyter notebook to execute the ETL process.
Run the Crowdfunding_ETL.sql file to create the tables in the Postgres database.

## Conclusion

With this project, we successfully transformed raw crowdfunding data into usable tables that can be queried in a Postgres database. The process involved using the pandas library to clean the data, creating separate tables for category and subcategory, and using SQL to create the tables in Postgres.
