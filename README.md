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
5. *Step 5* - Interprete and share the results

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

                        Data Manipulation Techniques

  - Recoding data - is a technique you can use to map original values for a variable into new values to facilitate analysis. Recoding groups data into multiple categories, creating a categorical variable. A categorical variable is either nominal or ordinal. Nominal variables are any variable with two or more categories where there is no natural order of the categories, like hair color or eye color. Ordinal variables are categories with an inherent rank
 
  - Derived Variables - is a new variable resulting from a calculation on an existing variable.
 
  - Data Merge- uses a common variable to combine multiple datasets with different structures into a single dataset. Merging data improves data quality by adding new variables to your existing data.
 
  - Data Blending - combines multiple sources of data into a single dataset at the reporting layer.
 
  - Concatenation -  the merging of separate variables into a single variable. Concatenation is a highly effective technique when dealing with a source system that stores components of a single variable in multiple columns.
 
  - Data Append - combines multiple data sources with the same structure, resulting in a new dataset containing all the rows from the original datasets. When appending data, you save the result as a new dataset for ongoing analysis.
 
  - Imputation - is a technique for dealing with missing values by replacing them with substitutes. When merging multiple data sources, you may end up with a dataset with many nulls in a given column. If you are collecting sensor data, it is possible to have missing values due to collection or transmission issues.

*Few approaches an analyst can use for imputing values:* - 
1. remove Missing Data - remove the missing rows with missing values without impacting the quality of your overall analysis
2. replace with zero - replace missing value with zero
3. replace with overall average - instead of using zero just use calculated overall average
4. replace with most frequent (Mode) - use most frequently occuring value
5. closet value average - use the value from the rows before and after the missing value
- Reduction - is the process of shrinking an extensive dataset without negatively impacting its analytical value.
- Dimensionality reduction - which removes attributes from a dataset. Removing attributes reduces the dataset's overall size
- Numerosity reduction - which reduces the overall volume of data.
      (i) Aggregation - is the summarizetion of raw data for analysis, means of controlling privacy
      (ii) Transposition - is when you want to turn rows into columns or columns into rows to facilitate analusis.
      (iii) Normalization - converts data from different scales to the same scale
      (iv) Min - Max Normalization - Straightforward approaches to normalization
      (v) Parsing / String -

# *Managing Data Quality*
                        Circumstances to Check for Quality
Types of quality issues that can occur and have an overarching strategy to ensure the quality of your data.
1. Data Acquisition
2. Data Transformation and Conversion
3. Data Manipulation
4. Final product Preparation

                        Automated Validation
Automated data validation is faster and more accurate than manual methods. Automated data validation tools catch more existing errors and eliminate human error.

                        Data Quality Dimensions
it is essential to  consider multiple attributes of data when considering its quality.
                        Six dimensions of data quality 
1. Data Accuracy
2. Data Completeness
3. Data Consistency
4. Data Timeliness
5. Data Uniqueness
6. Data Validity

                        Data Quality Rules and Metrics
With an understanding of data quality dimensions, you need to consider how to measure each of them in your quest to improve overall quality. Let's consider data conformity, which encompasses elements of accuracy, consistency, uniqueness, and validity. When consolidating data from multiple source systems into an analytics environment, one factor you want to assess is the conformity or nonconformity of data. If source data does not match the destination data type size and format, you have nonconformity.

                        Methods to Validate Quality
A sound approach to ensuring and improving data quality is by combining these methods appropriately.
(i) Reasonable Expectations - s to determine whether or not the data in your analytics environment meets your reasonable expectations.
(ii) Data Profiling - is to improving quality is to profile your data. Data profiling uses statistical measures to check for data discrepancies, including values that are missing, that occur either infrequently or too frequently, or that should be eliminated. Profiling can also identify irregular patterns within your data.
(ii) Data Audits -  to keep in mind is auditing your data. Data audits look at your data and help you understand whether or not you have the data you need to operate your business. Data audits use data profiling techniques and can help identify data integrity and security issues.
(iv) Sampling - for validating data quality is by examining a sample of your data. Sampling is a statistical technique in which you use a subset of your data to inform conclusions about your overall data.
(v) Croos-Validation - use existing data to generate predictive models using a variety of statistical methods. Cross-validation is a statistical technique that evaluates how well predictive models perform. Cross-validation works by dividing data into two subsets. The first subset is the training set, and the second is the testing, or validation, set.

# Chapter 5
# Data Analysis and Statistics.
      Fundamentals of statistics

Common Symbols in Statistics

There are two kinds of statistics
(i) Inferential Statistics
(ii) Descriptive Statistics

            Inferential Statistics
Deals with taking a sample and analyze that sample and making judgmental claims about the population.

            Descriptive Statistics
Get data and talk about it

*What is popualation?*
refers to the total amount of "THINGS"

*What is a sample?*
Refers to a small part of the population that is used for study.
- sample size - Total amount of the "THINGS" in a sample.

*What we examine is variable*
What we are studying and it can be measurable, countable and catagorized.
we measure variable
      Quantitative or categorical.

 # Descriptive Statistics
is a branch of statistics that summarizes and descibes data.

Measures of frequency
-help you nderstand how often something happens
1. Count - understand how much data you're working with is to count the number of observations.
2. Percentages - is a frequency measure that identifies the proportion of a given value for a variable with respect to the total number of rows in the dataset.
3. Frequency - describes how often a specific value for a variable occurs in a dataset.

   Measures of Central Tendency
help to establish an overall perspective on a given dataset, an analyst explores various measures of central tendency.
1. Mean- mean/ average. add all the numbers together then divide the total sum by the number of scored used.
2. Median - is the middle value in a set of data
3. Mode - is a number in a set of numbers that appears the most often.

   Measures of Dispersion
1. Range - the difference between the highest and the lowest values.
2. Interquartile range - tells you the spread of the middle half of your distribution.
3. Distribuion / propability distribution - is a function that illustrate probable values for a variables, and frequency with which they occur.

   Many possible shapes of Distributions

1. Normal Siatribution - is also know as bell-curve  is symmetricalli dispersed around its mean which gives it a distinctive bell-like shape
2. Skewed distribution - has an asymmetrical shape, with single pek, and long tail on one side. skewed have either a right (positive) or left (negative) skew. When skew is to the right the meean is typically greater than median. on the other hand with a left skew typically has a mean less than median.
3. Bimoodal Distribution - has two distinct modes, whereas a multimodal distribution has multiple distinct modes. When you visualize a bimodal distribution you see two separate peak.

   Variance
is a measure of dispersion that takes the values for each observation in a dataset and calculates how far away they are from that mean value.

 Standard Deviation
is the average deviation between individual values and the mean.

Each Sample is Unique
-keep in mind that each sample from a population is unique.
1. Special normal distributions - central limit theorem and empirial rule combine to makethe normal distribution is the most important distribution in statistics.

   Two special normal didtribution
1. Standard normal distribution or Z- distribution is a special normal distribution with a mean of 0 and a standard deviation of 1.
2. Students T-distribution - commonly know as the t-distribution is similar to the standard normal distribution in that it has a mean of 0 with bell-like shape.

         Inferential Statistics
is a branch of statistics that uses samples data to draw conclusions about the overall population.

Hypothesis Testing
-test consists of two statements, only one of which can be true.
1. Consists of two components  - (i) null hypothesis
                                 (ii) Alternative hypothesis
2. When designing a hypothesis test, you first develop the null hypothesis (h0), and it presumes that there is no effect on the test you are conducting.
3. Alternative hypothesis (Ha) presumes that the test you are conducting has an effect


   *(i) Hypothesis testing with the Z-test*
is appropriate when you have a sample size over 30 and a know population standard deviation, and you are using normal distribution

      *(ii) Hypothesis Testing with the T-test
frequently the standard deviation of the  population is unkown. its also possible that you will have sample size of less than 30.
Z-test and T-test work well for numeric data.

      *(iii) Hypothesis testing with Chi-Square
is available when you need to assess the association of two catagorical variables.

Simple Linear regression
- is an analysis technique that explores the relationship between an independant variable and dependan variable.

  Multiple Linear Regression
- builds on that concept by examine effect of numerous independent variable on dependent variable.

# Analysis Techniques
Types of Analysis
1. Trend - compare data overtime.
2. Perfomance - assesses measurements against defied goals.

   Explorig Data Analysis (EDA)

steps to follow when conucting a EDA.
1. Check data structure - ensure that data  is in the correct format for analysis
2. Check data representation - become familiar with data
3. Check if data is missing - check to see if any data is missing from the dataset and determine what to do next.
4. Identify outliers - determine the cause of outliers and consider whether you want to leave them in the data before proceeding with any ongoing analysis.
5. Summarize statistics - calculate summary statistics for each variable.
6. check assumptions -

# Module 3
# Chapter 6 
Data Analytics Tools:
(i) Spreadsheets - is the most widely used tool in the world of analytics
(ii) Microsofy Excel - is the most commonly used desktop speadsheet application.

Programming Languages
1. R - it is focused on craeting analytics application
2. Python - is general-programming language
3. Structured Query Language(SQL)- language of database
   *sub langusages*
1. Data Definition Language(DDL) - it is used to the structure of the dtabase itself.
2. Data manipulation Languages(DML) - subset of SQLcommands that are used to work with the data inside of a database. they do nt change the database structure but they add, remove, and change the data inside a database.

   DDL Commands
1. Create - create new table withing database/ new database.
2. ALTER - change the structure of  table that you've created.
3. DROP - delete the entire table or database from your server.
   
   DML commands
1. SELECT- retrieve information from database
2. INSERT - add new records to a database table
3. UPDATE - modify rows in the database
4. DELETE - dalate rows from a database table

Statistics Packages
1. IBM SPSS -
2. Stata - less widely used than the more popular SPPS tools
3. Minitab -

      Machine Learning Tools
1. IBM SPSS MODELER -
2. RAPIDMINER -

      Analytics Suites
1. IBM Cognos -
   major components of cognos includes:-
   1. Cognos connection - wen-based portal thatoffers access to other elements o cognos suites
   2. Query studion - provides access to data query and basic reporting tools.
   3. Reporting studio - offers advanced report design tools for complex reporting needs.
   4. Analysis studio - enables advanced modeling and analytics on large datasets
   5. Event stuido - provide real-time data monitoring
   6. Metric studio - abality to create scorecards for business
   7. Cognos Viewer - allows stakeholders to easily interact
  
Microsoft Power BI
1. Power BI desktop - interact with data and publish
2. Power BI - hosts Power BI capabilities in he cloud
3. Mobile apps - Provide users of devices with access
4. Power BI report builders - allow developer to create
5. Power BI report server - hosts Power BI environment

   Micro Strategy
-is less well-know than similar tools from IBM and microsoft, but it does have a well-establish user base
1. Demo - is SaaS that allows businesses to ingest their data and apply a variety of analytic and modeling cap.
2. Datorama - is an analytics tools that focuss on a specific component of an oeganization business sales and marketing.
   
# Chapter 8
# Data-Governance
Data governance is the set of policies, procedures, and controls that an organization develops to safeguard its information while making it useful for transactional and analytic purposes. As the name implies, data governance is primarily a business function. Governments have a method for creating, interpreting, and enforcing laws. 

 # Data Governance Roles
- Data stewardship is the act of developing the policies and procedures for looking after an organization's data quality, security, privacy, and regulatory compliance. The data steward is responsible for leading an organization's data governance activities. As the link between the technical and non-technical divisions within an organization, a data steward works with many people, from senior leaders to individual technologists. To establish policies, a data steward works with various data owners.
- Data owner is a senior business leader with overall responsibility for a specific data domain. A data domain, or data subject area, contains data about a particular operational division within an organization. Data owners work with the data steward to establish policies and procedures for their data domain.
- Data custodian is a role given to someone who implements technical controls that execute data governance policies. Data custodians are frequently information technology employees who configure applications, dashboards, and databases.
- Data access requirements determine which people need access to what data. Access requirements differ by data subject area and can be as granular as a single.
- A data classification matrix defines categories, descriptions, and disclosure implications for data.

  # Access Permissions
It is a best practice to use role-based access to grant people permission to access data. Role-based access means that instead of giving access to individual people, you grant access to the role they occupy. When you define roles and then assign people to those roles, it simplifies how you manage permissions.

 # Group Permissions 
 When developing a role-based access strategy, it is common to implement user group-based permissions. 

  # Data Use Agreements
A data use agreement (DUA) is a contractual document for transferring private data between organizations. You should establish a DUA before sharing data with an outside party. It is essential to understand the classification for each piece of data when crafting a DUA. 
A DUA provides details governing the transfer, use, and disclosure of reporting protocols for the data. Some of these details are:

- Identifying who will receive the data
- Identifying how the data can be used
- Prohibiting the further distribution of the data
- Establishing the method of transfer
- Identifying how the recipient will protect the data

 # Security Requirements
- Encryption
- Data in transit is data that is actively moving between one location and another.
- Data masking, or data obfuscation, replaces sensitive information with a synthetic version.
- Deidentifying data is the process of removing identifiers that can compromise individual privacy. How you deidentify depends on your use case. One way of deidentifying data is to share only aggregated or summarized data. Another way is to remove variables from the data.
- Reidentifying data happens when you take deidentified datasets and join them in a way that establishes the identity of individuals. For example, you can identify most Americans by combining their birth date, sex, and zip code.

  # Storage Environment Requirements
There are many environments where data at rest exists, including local storage, a shared drive, and the cloud. Regardless of the storage environment, you need to encrypt all data at rest. Local storage is the storage media on an individual device, such as a hard drive in a laptop. Encrypting local storage is straightforward, regardless of the operating system you use.

 # Use Requirements

Use requirements specify how to collect, process, use, store, retain, and remove data. While understanding audience requirements is vital for creating impactful visualizations, understanding data use requirements is crucial to effective data governance. An *acceptable use policy* (AUP) defines an individual's responsibilities when accessing, using, sharing, and removing organizational data. While an AUP is a document with a broad scope, it has provisions for each type of data in an organization's data classification matrix. AUPs describe acceptable locations for storing proprietary information; what to do in the event of theft, loss, or unauthorized disclosure; and methods of disposal.

 # Data Classification Requirements
IData classification is the process of analyzing data and organizing it into risk-based categories. Classifying data is appropriate for both structured and unstructured data. 
- Personally Identifiable Information (PII) is any data that can uniquely identify a person and the information below can be applied to other countries. PII is any information about an individual maintained by an agency, including (1) any information that can be used to distinguish or trace an individual's identity, such as name, social security number, date and place of birth, mother's maiden name, or biometric records; and (2) any other information that is linked or linkable to an individual, such as medical, educational, financial, and employment
- Protected Health Information Under HIPAA, Protected Health Information (PHI) is the broad category of data elements identifying an individual's health information. This information can be about the individual's past, current, or future health status and covers providing healthcare, processing healthcare payments, or processing insurance claims. Alternatively, Electronic Protected Health Information, or e-PHI, is any PHI you store or transmit digitally.

  # Payment Card Information
The Payment Card Industry (PCI) is a non-governmental body that governs card-based financial payments. To protect the integrity of card-based financial transactions and prevent fraud, leading financial service companies, including MasterCard, Visa, Discover, American Express, and the Japan Credit Bureau, created the PCI Security Standards Council (PCI SSC). The PCI SSC develops policies to govern the processing, transmission, and storage of electronic payments.

The PCI Data Security Standard (PCI DSS) is the industry's core information security standard. The following six principles encompass the objectives set out by the PCI DSS:

- Building and maintaining a secure network
- Protecting cardholder data
- Maintaining a vulnerability management program
- Implementing strong access controls
- Regularly monitoring and testing networks
- Maintaining an information security policy
The second category is Sensitive Authentication Data (SAD). SAD includes complete track data from the magnetic stripe or embedded chip, Personal Identification Number (PIN), and the Card Verification Value (typically three digits on the back of a card).

# Jurisdiction Requirements
These categories include criminal law, civil law, administrative law, and private regulations.
- The goal of *criminal law* is to discourage people from acting in a way that negatively impacts society.
- The goal of civil law is to resolve disputes between individuals, organizations, and government agencies.
- The goal of administrative law is to enable the effective operation of government by allowing government administrative agencies to propagate regulations.
- The goal of private industry regulations is to govern the activities of individuals and organizations without the force of law. 

# Understanding Master Data Management
Master data management (MDM) is a data governance discipline that uses processes, tools, and technologies to ensure that data assets across an organization have a single source of truth. Successfully implementing MDM is a challenge regardless of industry or organizational size. As organizational complexity increases, identifying and maintaining an accurate, consistent, well-governed single source of truth becomes more challenging.

# Processes
The discipline of MDM is process-centric. For an organization with multiple separate operational systems, the consolidation of multiple data fields is part of a comprehensive duplicate resolution process. Maintaining a data dictionary is an essential component of effective MDM. A data dictionary is a document that contains metadata about your data structures.
In addition to the details about each column in the table, a data dictionary includes other metadata, including

Purpose of the table
Primary/foreign keys
Column index definitions
References by internal systems
References by external systems
Maintaining a data dictionary takes a significant effort. Fortunately, tools exist that can extract most of the metadata about tables from a database. It is crucial to instill procedural discipline for maintaining column-level comments since they help orient new analysts to your systems.

# Circumstances

Many circumstances lead an organization to pursue MDM. Typically, leadership identifies a difficulty that relates to having consistent information. To improve internal efficiency and reduce data quality issues, leadership recognizes the benefits of enhancing consistency across systems. 

Another reason for adopting MDM is compliance with policies and regulations that require consistent handling of data. When the same data has different definitions in different systems, the cost of compliance increases. Using MDM to drive accurate and consistent data definitions leads to better data stewardship, which drives down the cost of compliance.






  
