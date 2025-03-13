# Overview

This project is focused on data cleaning for a customer call list using Python and Pandas. The dataset is read from an Excel file (Customer Call List.xlsx), and various preprocessing steps are applied to ensure data quality, consistency, and usability.

# Dataset

The dataset contains a list of customer calls with the following columns:

CustomerID: Unique identifier for each customer.

First_Name: First name of the customer.

Last_Name: Last name of the customer (1 missing value).

Phone_Number: Contact number (2 missing values, inconsistent formats like 123-545-5421, 123/643/9775, 7066950392).

Address: Full address (could be split into Street, City, Zip Code).

Paying Customer: Indicates if the customer is paying (Yes, No, Y, N - needs standardization).

Do_Not_Contact: Flags customers who shouldn't be contacted (4 missing values, inconsistent values Yes, No, Y, N).

Not_Useful_Column: A boolean column that is likely unnecessary and should be removed.

# Features & Data Cleaning Steps

The Jupyter Notebook performs the following key data cleaning tasks:

Loading Data:

- The dataset is read using pandas.read_excel().

Handling Missing Data:

- Identifying missing values in Last_Name, Phone_Number, and Do_Not_Contact.

- Filling or dropping null entries where necessary.

Standardizing Data Formats:

- Formatting phone numbers to a uniform structure (removing special characters like -, /, |).

- Standardizing date formats (if applicable).

Removing Duplicates:

- Detecting and dropping duplicate records to ensure data accuracy.

Cleaning Text Fields:

- Stripping unnecessary characters and spaces.

- Converting text to a consistent case (e.g., lowercase or title case).

Standardizing Categorical Data:

- Converting Paying Customer to consistent values (Yes → Y, No → N).

- Converting Do_Not_Contact values (Yes, No, Y, N → standardized format).

Dropping Unnecessary Columns:

- Removing Not_Useful_Column since it doesn't contribute to the analysis.

Exporting Cleaned Data:

- Saving the cleaned dataset as a new Excel or CSV file for further analysis.
