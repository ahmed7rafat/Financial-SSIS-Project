# Financial-SSIS-Project

**Project Overview**

This SSIS project demonstrates a complete ETL (Extract, Transform, Load) pipeline designed to integrate financial and customer data from multiple sources — SQL Server, Excel, and CSV — into a unified SQL Server database for business analysis and reporting.

The goal is to combine purchase data, currency exchange rates, and customer contact information into a single, clean, and well-structured table.

**Business Request**

The business has customer purchase data stored in local currency and needs it converted to a standard currency (USD).
Additionally, customer contact information needs to be combined with purchase data for unified reporting.

Data sources:

Purchase data → stored in SQL Server

Currency conversion rates → stored in Excel file

Customer contact information → stored in CSV file

Task:
Bring all data together in a new SQL Server database for the business.

**Implementation Steps**

Project Setup

Created a new SSIS Project in Visual Studio (SQL Server Data Tools).

Configured connections for SQL Server, Excel, and Flat File (CSV) sources.

Data Extraction

Imported purchase data from SQL Server.

Imported exchange rate data from Excel.

Imported customer data from CSV file.

Data Transformation

Used Lookup Transformation to match and convert local currency to USD.

Applied Derived Column to calculate converted amounts.

Implemented Data Conversion to fix data type mismatches.

Used Conditional Split to handle rows with missing or invalid data.

Applied Union All to combine multiple data streams.

Error Handling & Debugging

Configured Data Viewers to debug transformations.

Managed missing lookup matches using No Match Output.

Added handling for duplicate and null data during transformation.

Data Loading

Loaded the final transformed data into a new SQL Server destination table.

Ensured data integrity and proper mapping of all columns.

**Key Learnings**

Building ETL pipelines using SQL Server Integration Services (SSIS).

Working with multiple data sources (SQL, Excel, CSV).

Implementing Lookups, Derived Columns, Conditional Splits, and Error Handling.

Understanding data conversion and transformation logic in financial contexts.

**Tools & Technologies**

SQL Server Integration Services (SSIS)

SQL Server Management Studio (SSMS)

Microsoft Excel

CSV Flat Files

Visual Studio (SSDT)

**Output**

A consolidated SQL Server table that contains:

Customer purchase details

Converted currency amounts (in USD)

Customer contact information

This final dataset enables the business to perform accurate financial analysis and reporting across unified data sources.
