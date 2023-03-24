# Crowdfunding ETL

This project is focused on extracting, transforming, and loading data from a crowdfunding dataset into a Postgres database.

## Tools used

Python,
Pandas library,
Postgres,
Jupyter Notebook

## The data cleaning process involved the following steps:

Read in the crowdfunding.xlsx file using the pandas library and put data into a dataframe.
Split the Category and Subcategory column into two separate columns. 
Create separate dataframes for Category and Subcategory. Each dataframe will have two columns one listing the category or subcategory and the other with an ID column create using pandas. Use images below as an example.


![category_table](https://user-images.githubusercontent.com/94406047/227388080-a13fb1d2-bb37-4ea1-87a5-1928ea61d9cf.png)

![subcategory_table](https://user-images.githubusercontent.com/94406047/227389322-dfff432d-1525-40c2-961e-b39b041612b9.png)

Edit the Campaign table by dropping unnecessary columns and ensuring correct data types. Merge the Category ID and Subcategory ID columns into the Campaign table. To create one final dataframe like the image below.

![capaign_table](https://user-images.githubusercontent.com/94406047/227388220-42d3d0e6-713f-4fab-9335-fc14e2dcced2.png)

Read in the Contacts JSON file. Use a for loop to separate each row into columns by the "," delimiter, creating the Contacts dataframe with four columns. One for the contact_id, first_name, last_name and email. 

![contacts_table](https://user-images.githubusercontent.com/94406047/227388386-40334684-148f-45b4-9583-e44160d7041c.png)

For the database you should use postgres. Create a new database titled crowdfunding_db. Use SQL to create each table in Postgres, ensuring proper primary key and foreign key labels. You can use the crowdfunding_db_schema.sql file within this github repository to create the tables. All table are created with lowercase letters to insure consistency. Import the CSV file containing the data frames in the specific order: category, cubcategory, contacts, and campaign (last). It is important that the campaign table is last. 

## Files included

ETL_Mini_Project_JFabricatore.ipynb: Jupyter notebook containing the Python code for importanting and cleaning process.
crowdfunding_db_schema_sql: SQL file containing the code for creating tables in Postgres.
Resources: Folder containing the two raw data xlsx files and the four cleaned data frames that were exported.
Images: Folder containg all images used in the readme and examples of the postgres tables properly imported. 


## Conclusion

With this project, we successfully transformed raw crowdfunding data into cleaned data frame tables that can be queried in a Postgres database. The process involved using the pandas library to clean and export the data, creating separate tables for category and subcategory, contacts and campaign. Finally using SQL to create the tables in Postgres and importing the exported files into each table.  
