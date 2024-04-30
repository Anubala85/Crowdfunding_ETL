# Crowdfunding_ETL

**Contacts DataFrame**

- Used **option 2: Regex to create the contacts DataFrame**
    - Used findall with '\d+' to pull the 4 digit contact_id
    - Checked the datatypes
    - Converted the contact_id column to an int64 data type with astype () function
    - Used regex search '(?<=name\"\:\s\")(.*)(?=\",)' to extract the full name of the contact from contact_info.
    - Used regex search with '(?<=email\"\:\s\")(.*)(?=\")' to extract the email id from the contact_info.
    - Created a clean Dataframe with contact_id, name and email information as columns
    - Used regex split to create first name and last name columns within the df
    - dropped the full name column using df.drop()
    - Reorders the columns
    - The DataFrame has the following columns:
        - "contact_id" column
        - "first_name" column
        - "last_name" column
        - "email" column
    - The contacts DataFrame is exported as contacts.csv under the resources Folder.
 

## Time to create Crowdfunding Database
1.   Inspect all four CSV files generated:
      Campaign.csv
      Category.csv
      Contacts.csv
      Subcategory.csv
     to understand the different entities(tables) and the relationships between them. Identify the columns in each table that can act as primary keys(PK) and foreign keys(FK).
2.   Go to the QuickDBD website to sketch an ERD of the tables [QuickDBD](https://www.quickdatabasediagrams.com/)
3.   Defined the table structure by typing the table name followed by its columns and data types in the format table_name. Generated four tables for Campaign, Category, SubCategory and Contacts and establish the       relationships between the entities. Relationships show how the entities are connected to each other. In this case, contacts_id, Category_id and Subcategory_id columns in respective tables showed connection         with Campaigns table.
4.   Once mapped out all the entities and relationships, review your ERD for accuracy. Then, you can export the diagram in the desired format such as PostgreSQL, SQL Server, pdf documentation or PNG and so on.
5.   Save the PostgreSQL script with the table schemas as crowdfunding_db_schema.sql.
6.   Open pgAdmin and connect to your server. Create a new database named crowdfunding_db.
7.   Open a query tool in pgAdmin connected to the crowdfunding_db. Execute the SQL script containing the table schemas to create the tables in the correct order.
8.   Import each CSV file into its corresponding SQL table in the crowdfunding_db database
9.   Run a SELECT statement for each table to verify that each table has the correct data.
10.   Specify the Delimiter and Quote character based on the format of your CSV file. Ensure that the Header option is set correctly if your CSV file has a header row.
11.   By following these steps, you will be able to sketch an ERD, create table schemas, set up a PostgreSQL database, create tables, import data, and verify the correctness of the tables and data.

