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


---

## 🏬 Real-World Use Case (CCTV Retail Example)
This database is tailored for electronic retail businesses, such as a **CCTV Camera & Security Systems Store**. 
* **Product Table:** Tracks inventory items like *Hikvision 4MP Domes, Dahua PTZ Cameras, and 8-Channel DVRs*.
* **Product_Sales Table:** Acts as the checkout system, recording everyday customer transactions and quantities sold.

---

## 🚀 How to Run & Setup
1. Clone this repository or download the `.sql` script file.
2. Open Microsoft SQL Server Management Studio (SSMS) and log into your local instance.
3. Open a **New Query** window, paste the script, and press **Execute (F5)** to auto-generate the schema, primary-foreign key relationships, and seed data.
4. Run the **Advanced Multi-Table JOIN Query** provided above to instantly generate your first sales report!
