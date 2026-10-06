HBase Customer 360 / Customer Profile
1. Project Overview

This project demonstrates a Customer 360 / Customer Profile use case using Apache HBase.

A telecom company needs fast access to customer information such as Customer ID, name, city, mobile number, plan, status, and data usage.

HBase is suitable because customer information can be retrieved quickly using the Customer ID as the RowKey.

2. Business Problem

A telecom company has millions of customers and needs to quickly retrieve an individual customer's profile.

The system stores:

Customer ID
Customer Name
City
Mobile Number
Plan
Status
Data Usage
3. Technology Used
Apache HBase
Hadoop HDFS
Linux
HBase Shell
4. HBase Table Design

Table Name: customer_profiles

RowKey: Customer ID

Column Family: info

Example:

RowKey: CUST1001

info:name
info:city
info:mobile
info:plan
info:status
info:data_usage
5. Operations Demonstrated

The project demonstrates the following HBase operations:

Create table
Insert customer data using put
Retrieve a customer using get
Display all customers using scan
Count records using count
Delete data
Describe table
Disable and drop table
6. Example Commands

Create the table:

create 'customer_profiles', 'info'

Insert customer data:

put 'customer_profiles', 'CUST1001', 'info:name', 'Jay'
put 'customer_profiles', 'CUST1001', 'info:city', 'Pune'
put 'customer_profiles', 'CUST1001', 'info:mobile', '9876543210'
put 'customer_profiles', 'CUST1001', 'info:plan', 'Premium'
put 'customer_profiles', 'CUST1001', 'info:status', 'Active'
put 'customer_profiles', 'CUST1001', 'info:data_usage', '25GB'

Retrieve a customer:

get 'customer_profiles', 'CUST1001'

Display all customers:

scan 'customer_profiles'

Count customers:

count 'customer_profiles'
7. Project Flow
Customer ID
     |
     v
+-------------------+
|       HBase       |
| customer_profiles |
+-------------------+
     |
     v
Customer Information
(Name, City, Mobile,
 Plan, Status, Usage)
8. Result

The project successfully demonstrates how HBase can be used to store and quickly retrieve customer profiles using the Customer ID as the RowKey.

9. Learning Outcome

This use case provides practical experience with:

HBase table creation
RowKeys
Column Families
CRUD operations
HBase Shell
Fast customer lookup
Scanning and counting records
