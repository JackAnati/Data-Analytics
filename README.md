# Data-Analytics

# Module 1: The Basics of Data 

# Chapter 1
*What is Data Analytics?*
Convert raw data into actionable insghts that guide decision-making processes within an organization.

*What is used for?*
used to make faster, Better and Business decision - 1. To reduce overall business costs, 2. Develop new and innovative products and servvices.

Might use to the following -
1. To predict future sales or purchasing behavious
2. To help and protect against fraud
3. To analyze the effectiveness of marketing campaigns
4. To boost customer acquisition and retention
5. To increase supply chain efficiency

FIVE MAIN STEPS OF DATA ANALYTICS
would take when approaching a new project
1. *Step 1* - Define the questions
2. *Step 2* - Collect the data
3. *Step 3* - Clean the data
4. *Step 4* - Analyze the data
5. *Step 5* - Intrprete and share the results

# golden Age of Analytics
are Data, Storage, and/or Computing



# Several key responsibilities and skills.
1. Data Collection and Preparation
2. Data Analysis
3. Data Visualization and Storytelling
4. Decision Support
5. Coolaboration and Communication
6. Continuous Learning and adaptation



# Chapter 2 
*Exploring Data Types*
- A *data element* is an attribute about a person, place, or thing containing data within a range of values. Data elements also describe characteristics of activities, including orders, transactions, and events.
- A *data type* limits the values a data element can have. 

*Tabular Data*
- Tabular data is data organized into a table, made up of columns and rows.

# *Structured data*
- Structured data is tabular in nature and organized into rows and columns. Structured data is what typically comes to mind when looking at a spreadsheet.

*Character*
-The character data type limits data entry to only valid characters. Characters can include the alphabet that you might see on your keyboard, as well as numbers. Depending on your needs, multiple data types are available that can enforce character limits.
- Alphanumeric is the most widely used data type for storing character-based data. As the name implies, alphanumeric is appropriate when a data element consists of both numbers and letters

*Character Sets*

When considering alphanumeric and text data types, you need to think about the character set you are using to input and store data when using a database. Databases use character sets to map, or encode, data and store it digitally

*Strong And Weak Typing*

Weak typing loosely enforces data types. Spreadsheets use weak typing to help make it easier for people to accomplish their work. Spreadsheets default to an “automatic” data type and accommodate practically any value. When a person specifies a data type, it is loosely enforced compared to a database. For example, with a numeric spreadsheet cell, the software does not stop you from entering and storing characters.

# *Unstructured data*
While much of the data we use to record transactions is highly structured, most of the world's data is unstructured. Unstructured data is any type of data that does not fit neatly into the tabular model. Examples of unstructured data include digital images, audio recordings, video recordings, and open-ended survey responses. Analyzing unstructured data creates a wealth of information and insight. 

# *Categories of Data*
We try to fit data into structured and unstructured categories. The reality is that the world is not black and white, and not all data fits neatly into structured and unstructured categories. Semi-structured data represents the space between structured spreadsheets and unstructured videos.

# Text file
In addition, many coding languages have libraries that make it easy to write comma- or tab-delimited files. When a file is comma-delimited, it is known as a comma-separated values (CSV) file. Similarly, when a file is tab-delimited, it is called a tab-separated values (TSV) file.

# Module 2: Data Preparation and Exploration
# Chapter 3
# Exploring Database
Two main database catagories:
(i) Relational
(ii) Non-relational

Benefits of Relational Model
(i) Consistency
(ii) Security
(ii) Ease back-up and recovery

Nonrelational Model

Different types of nonrelational database
(i)Key value
(ii) Column store
(iii) Graph
(iv) Document store

Benefits
(i) Flexibility
(ii) Scalability 
(iii) Cost effectiveness

# Database Use Cases
Databases tend to support two major categories of data processing: Online Transactional Processing (OLTP) and Online Analytical Processing (OLAP).

*Online Transactional Processing*
OLTP systems handle the transactions we encounter every day. Example transactions include booking a flight reservation, ordering something online, or executing a stock trade. While the number of transactions a system handles on a given day can be very high, individual transactions process small amounts of data. OLTP systems balance the ability to write and read data efficiently.


# Normalization
Is a process for structuring a database in a way that minimize duplication of data.

*Three types of database normalization*
- 1NF - For a table to be in the first normal form, it must meet the following criteria:
      - a single cell must not hold more than one value (atomicity)
      - There must be a primary key for identification
      - No duplicated rows or columns
      - Each column must have only one value for each row in the table.
- 2NF - The 1NF only eliminates repeating groups, not redundancy. That’s why there is 2NF.
      - It’s already in 1NF
      - Has no partial dependency. That is, all non-key attributes are fully dependent on a primary key.
- 3NF - When a table is in 2NF, it eliminates repeating groups and redundancy, but it does not eliminate transitive partial dependency
      - be in 2NF
      - have no transitive partial dependency.

OLAP - *Online Analytical Processing*
OLAP systems focus on the ability of organizations to analyze data. While OLAP and OLTP databases can both use relational database technology, their structures are fundamentally different. OLTP databases need to balance transactional read and write performance, resulting in a highly normalized design. Typically, OLTP databases are in 3NF.

# Schema Concept

A *data mart* is a subset of a data warehouse. Data warehouses serve the entire organization, whereas data marts focus on the needs of a particular department within the organization. For example, suppose an organization wants to do analytics on their employees to understand retention and career evolution trends. To satisfy that use case, you can create a data mart focusing on the human resources subject area from the data warehouse. 
A *data lake* stores raw data in its native format instead of conforming to a relational database structure. Using a data lake is more complex than a data warehouse or data mart, as it requires additional knowledge about the raw data to make it analytically useful. Relational databases enforce a structure that encapsulates business rules and business logic, both of which are missing in a data lake.

# Data Acquisition Concepts
To perform analytics, you need data.

Difference between Database, Data warehouse, and Data Lake?

                        Database 
- Designed to capture and record OLTP
- Live, real-time data
- Refer to relational database
- Stored in table
- Data highly detailed
- flexible schema

                        Data warehouse
- Designed for analytical processing OLAP
- Data is summarized
- Rigid Schema. (how data is organized)
- Data is refreshed from source systems - store current and hestorical.

                        Data Lake
- Designed to capture data.
- Made for large amounts of data.
- Used for ML and AI in its current state or for analytics with processing
- Can organize and put into database or Data warehouse

                        *Integration*
Data from transactional systems flow into data warehouses and data marts for analysis. Recall that OLTP and OLAP databases have different internal structures. You need to retrieve, reshape, and insert data to move data between operational and analytical environments. You can use a variety of methods to transfer data efficiently and effectively.

One approach is known as extract, transform, and load (ETL). As the name implies, this method consists of three phases:
Extract, load, and transform (ELT) is a variant of ETL.
Extract:  In the first phase, you extract data from the source system and place it in a staging area. The goal of the extract phase is to move data from a relational database into a flat file as quickly as possible.
Transform:  The second phase transforms the data. The goal is to reformat the data from its transactional structure to the data warehouse's analytical design.
Load:  The purpose of the load phase is to ensure data gets into the analytical system as quickly as possible.


                        Data Manipulation
1. Create new data      - INSERT - creates
2. Read existing data   - SELECT - retrieves
3. Update existing data - UPDATE - changes
4. Delete existing data - DELETE - removes
            SELECT <what>
            FROM <source>
                        SQL Considerations
The keywords in SQL are case-insensitive. Howeever the case-sensitivity of column names and values depend on the database configuration.

                        Filtering
Add WHERE    SELECT FROM WHERE

                        Filtering and logical Operations
Add AND      SELECT, FROM, WHERE, AND

                        Sorting
Add ORDER BY      SELECT, FROM, WHERE, AND, OEDER BY

ASC  - ascending order
DESC - descending

                        Aggregate Functions
Summarized data helps quesions that executes have and aggregate functions are easy way. Also use aggregate function to filter data.

                        Coomon SQL aggregate Functions
1. COUNT  - returns the total number of rows of a query
2. MIN    - returns the minimum value from the results of a query
3. MAX    - returns the maximum value from the results of a query
4. AVG    - returns the mathematics average of the results of a query
5. SUM    - returns the sum of the results of a query
6. STDDEV - returns the sample standard deviation of results of a query

                        Logical Functions
Logical functions can make data substitutions when retrieving data. Remember that a SELECT statement only retrieves data. The data in the underlying tables do not change when a SELECT runs. 
                               The IFF function has the following syntax:
IFF(boolean_expression, true_value, false_value)
As you can see from the syntax, the IFF function expects the following three parameters:

1. Boolean Expression:  The expression must return either TRUE or FALSE.
2. True Value:  If the Boolean expression returns TRUE, the IFF function will return this value.
3. False Value:  If the Boolean expression returns FALSE, the IFF function will return this value.


# Chapter 4
# Data Quality
                  Data Quality Challenges

- Data Duplication - occurs when data representing the same transaction is accidentally duplicated within a system. To resolve duplicate data issues, the company has a duplicate resolution process.
- Redundant Data - redundant data happens when the same data elements exist in multiple places within a system. Frequently, data redundancy is a function of integrating multiple systems. Another root cause of data redundancy is an inappropriate database design.
- Missing value - Another issue that impacts data quality is the concept of missing values. Missing values occur when you expect an attribute to contain data but nothing is there. Missing values are also known as null values. A null value is the absence of a value. A null is not a space, blank, or other character. There are situations when allowing nulls makes sense. To handle missing values, you first have to check for their existence. SQL offers functions to check for null and functions that can replace a null with a user-specified value. There are similar functions in both Python and R.
- Invalid data - Invalid data are values outside the valid range for a given attribute. An invalid value violates a business rule instead of having an incorrect data type. As such, you have to understand the context of a system to determine whether or not a value is invalid.
- Nonparametric Data - s data collected from categorical variables, which you read about in Chapter 2: Understanding Data. Sometimes the categories indicate differentiation, and sometimes they have a rank order associated with them. In this latter case, the rank order of the values is of significance, not the individual values themselves.
- Data outliers - is a value that differs significantly from other observations in a dataset.
- Specification Mismatch - describes the target value for a component. A specification mismatch occurs when an individual component's characteristics are beyond the range of acceptable values.
- Data Type Validation - ensures that values in a dataset have a consistent data type. 

