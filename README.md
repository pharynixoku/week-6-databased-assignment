Week 6 Assignment: SQL Joins and RelationshipsOverviewThis repository contains the SQL solutions for the Week 6 Assignment: SQL Joins and Relationships. The queries demonstrate how to perform relational joins (INNER JOIN, LEFT JOIN, RIGHT JOIN) using the MySQL Classic Models database schema.Solutions BreakdownQuestion 1: INNER JOIN – Employees and OfficesRetrieves employee contact details alongside their office code using an INNER JOIN.SELECT 
    e.firstName,
    e.lastName,
    e.email,
    e.officeCode
FROM 
    employees AS e
INNER JOIN 
    offices AS o ON e.officeCode = o.officeCode;
Question 2: LEFT JOIN – Products and Product LinesRetrieves product details and their corresponding product lines using a LEFT JOIN.SELECT 
    p.productName,
    p.productVendor,
    p.productLine
FROM 
    products AS p
LEFT JOIN 
    productlines AS pl ON p.productLine = pl.productLine;
Question 3: RIGHT JOIN – Customers and OrdersRetrieves order dates, shipping status, and customer numbers for the first 10 orders using a RIGHT JOIN.SELECT 
    o.orderDate,
    o.shippedDate,
    o.status,
    o.customerNumber
FROM 
    customers AS c
RIGHT JOIN 
    orders AS o ON c.customerNumber = o.customerNumber
LIMIT 10;
File StructureFileDescriptionanswer.sqlContains all formatted SQL queries for Questions 1, 2, and 3.README.mdOverview and documentation of the repository solutions.ExecutionLoad the classicmodels database into MySQL Workbench.Execute the queries directly from answer.sql.
