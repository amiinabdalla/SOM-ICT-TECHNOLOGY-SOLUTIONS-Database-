# 🛒 Retail Store SQL Database System

Welcome to my first official SQL Database project! This database model is fully structured to manage sales, customers, and product inventories efficiently for a retail store business.

## 📊 Database Schema & Design
The database consists of three interrelated tables designed using Relational Database management practices:
* **Customer Table:** Stores customer profiles (`CustomerID`, `fullname`, `phone`, `address`).
* **Product Table:** Manages store inventory (`ProductID`, `productname`, `price`).
* **Product_Sales Table (Bridge):** Records transactions (`SaleID`, `customerid`, `productid`, `quantity`).

## 🚀 Advanced Multi-Table JOIN Query
This query connects all 3 tables to generate a comprehensive sales report showcasing the Customer Name, Product Name, and Quantity sold:

```sql
SELECT C.fullname, Pr.productname, S.quantity 
FROM Product_Sales S
JOIN Customer C ON S.customerid = C.customerid
JOIN Product Pr ON S.productid = Pr.productid;
