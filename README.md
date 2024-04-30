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
