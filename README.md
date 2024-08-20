## Project 2: Crowdfunding_ETL

Instructions
----------------------
The instructions for this mini project are divided into the following subsections:
1. Create the Category and Subcategory DataFrames
2. Create the Campaign DataFrame
3. Create the Contacts DataFrame
4. Create the Crowdfunding Database

Create the Category and Subcategory DataFrames
----------------------
1a. Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:
- A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories
- A "category" column that contains only the category titles

![category_df_snip](https://github.com/tgrishanina/Crowdfunding_ETL/blob/alanis/Images/category_df_snip.png)

2a. Export the category DataFrame as category.csv and save it to your GitHub repository.
3a. Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:
- A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories
- A "subcategory" column that contains only the subcategory titles

![subcategory_df_snip](https://github.com/tgrishanina/Crowdfunding_ETL/blob/alanis/Images/subcategory_df_snip.png)

4a. Export the subcategory DataFrame as subcategory.csv and save it to your GitHub repository.

Create the Campaign DataFrame
----------------------
2a. Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:
- "cf_id"
- "contact_id"
- "company_name"
- "blurb" (renamed to "description")
- "goal" (converted to a float data type)
- "pledged" (converted to a float data type)
- "outcome"
- "backers_count"
- "country"
- "currency"
- "launched_at" (renamed to "launch_date" and with the UTC times converted to the datetime format)
- "deadline" (renamed to "end_date" and with the UTC times converted to the datetime format)
- "category_id" (with unique identification numbers matching those in the "category_id" column of the category DataFrame)
- "subcategory_id" (with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame)

![campaign_df_snip](https://github.com/tgrishanina/Crowdfunding_ETL/blob/alanis/Images/campaign_df_snip.png)

2b. Export the campaign DataFrame as campaign.csv and save it to your GitHub repository.

Create the Contacts DataFrame
----------------------
3a. Choose one of the following two options for extracting and transforming the data from the contacts.xlsx Excel data:
- *Option 1: Use Python dictionary methods.
- Option 2: Use regular expressions.
3b. If you chose Option 1, complete the following steps:
- Import the contacts.xlsx file into a DataFrame.
- Iterate through the DataFrame, converting each row to a dictionary.
- Iterate through each dictionary, doing the following:
- Extract the dictionary values from the keys by using a Python list comprehension.
- Add the values for each row to a new list.
- Create a new DataFrame that contains the extracted data.
- Split each "name" column value into a first and last name, and place each in a new column.
- Clean and export the DataFrame as contacts.csv and save it to your GitHub repository.

![contact_info_df_snip](https://github.com/tgrishanina/Crowdfunding_ETL/blob/alanis/Images/contact_info_df_snip.png)


Create the Crowdfunding Database
----------------------
4a. Inspect the four CSV files, and then sketch an ERD of the tables by using QuickDBD
4b. Use the information from the ERD to create a table schema for each CSV file.
- Note: Remember to specify the data types, primary keys, foreign keys, and other constraints.
4c. Save the database schema as a Postgres file named crowdfunding_db_schema.sql, and save it to your GitHub repository.
4d. Create a new Postgres database, named crowdfunding_db.
4e. Using the database schema, create the tables in the correct order to handle the foreign keys.
4f. Verify the table creation by running a SELECT statement for each table.
4g. Import each CSV file into its corresponding SQL table.
4h. Verify that each table has the correct data by running a SELECT statement for each.

SQL Tables
----------------------
Contacts Table

![select_from_contacts](https://github.com/tgrishanina/Crowdfunding_ETL/blob/main/Images/select_from_contacts.png)


Campaign Table

![select_from_campaign](https://github.com/tgrishanina/Crowdfunding_ETL/blob/main/Images/select_from_campaign.png)


Category Table

![select_from_category](https://github.com/tgrishanina/Crowdfunding_ETL/blob/main/Images/select_from_category.png)


Subcategory Table

![select_from_subcategory](https://github.com/tgrishanina/Crowdfunding_ETL/blob/main/Images/select_from_subcategory.png)


All SQL Tables

![all_tables](https://github.com/tgrishanina/Crowdfunding_ETL/blob/main/Images/all_tables.png)