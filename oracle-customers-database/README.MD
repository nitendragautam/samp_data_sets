


##  OT Oracle sample database

This is an Oracle sample database named OT which is based on a global fictitious company that sells computer hardware including storage, motherboard, RAM, video card, and CPU.

You can see more details on this Original Location![Url](https://www.oracletutorial.com/getting-started/oracle-sample-database/)

The company maintains the product information such as name, description standard cost, list price, and product line. It also tracks the inventory information for all products including warehouses where products are available. Because the company operates globally, it has warehouses in various locations around the world.

The company records all customer information including name, address, and website. Each customer has at least one contact person with detailed information including name, email, and phone. The company also places a credit limit on each customer to limit the amount that customer can owe.

Whenever a customer issues a purchase order, a sales order is created in the database with the pending status. When the company ships the order, the order status becomes shipped. In case the customer cancels an order, the order status becomes canceled.

In addition to the sales information, the employee data is recorded with some basic information such as name, email, phone, job title, manager, and hire date.


#

## Oracle sample database diagram

![Database Diagram](/Oracle-Sample-Database.png)

Image source: In the Reference Section

The following illustrates the sample database diagram:

## Oracle Sample Database

|Table Names|	|Description	|Records
|:----------:|:----------------:|:--------|
|CONTACTS	|store contact person information of customers	|319 records|
 |COUNTRIES	|store country information|	25 records|
 |CUSTOMERS	|store customer master|	319 records|
 |EMPLOYEES	|store employee master|	107 records|
 |INVENTORIES|	store inventory information of products	|1112 records|
 |LOCATIONS	|store locations of warehouses	|23 records|
 |ORDERS	|store order header information|	105 records|
 |ORDER_ITEMS|	store order line items|	665 records|
 |PRODUCT_CATEGORIES|	store product categories|	5 records|
 |PRODUCTS	|store product information	|288 records
 |REGIONS	|store regions where the company operates|	4 records|
 |WAREHOUSES|	store warehouse information	9 records|


## Download Oracle Sample Database

You can download from below link or use the one in github repo.


https://cdn.oracletutorial.com/wp-content/uploads/2019/01/oracle-sample-database.zip


After downloading the file, you should extract it. The zip file contains the following *.sql files:

 (1)ot_create_user.sql is for creating OT user and grant privileges
 (2)ot_schema.sql is for creating database objects such as tables, constraints, etc.
 (3)ot_data.sql is for loading data into the tables.
 ot_drop.sql is for removing all objects in the sample database.


## Steps to Load the SQL file

### First Step: Use SQLplus to execute these scripts by using below syntax.

First Login using the existing Oracle user as a DBA and execute the sql queries from file.

```
SQL>@/path/to/my/query/myQueries.sql
SQL>/
```

### Second Step: First execute 1 and then change the user as below before executing 2. 

```
 $ORACLE_HOME/bin/sqlplus OT/admin123@//localhost:1521/xe
```

### Third Step: Execute SQL>@/path/to/query/ot_data.sql and Load the Data



### Fourth Step: Once the Data is loaded, you should be able to query it like below.

```
SELECT * FROM OT.employees;
```

```
EMPLOYEE_ID|FIRST_NAME|LAST_NAME |EMAIL                        |PHONE             |HIRE_DATE          |MANAGER_ID|JOB_TITLE                      |
-----------|----------|----------|-----------------------------|------------------|-------------------|----------|-------------------------------|
        107|Summer    |Payne     |summer.payne@example.com     |515.123.8181      |2016-06-07 00:00:00|       106|Public Accountant              |
        106|Rose      |Stephens  |rose.stephens@example.com    |515.123.8080      |2016-06-07 00:00:00|         2|Accounting Manager             |
        101|Annabelle |Dunn      |annabelle.dunn@example.com   |515.123.4444      |2016-09-17 00:00:00|         2|Administration Assistant       |
```


## Reference 

https://www.oracletutorial.com/getting-started/oracle-sample-database/
