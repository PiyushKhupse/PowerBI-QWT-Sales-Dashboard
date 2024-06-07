There are 13 tables: 
1 Categories: Category ID, Category Name,Description
2 Customers: Customer ID,Company Name,Contact Name,City ,Division,Address,fax,phone,postal code,state province
3 Divisions: Division Id, division Name
4 Employee Budget: Employee ID, target per employee
5 Employees: Employee ID,last name,first name,title,hire date,office date, office,extension,reports to,yearly salary
6 offices: office,office address,office postal code,office city,office state province,office phone,office fax,office country
7 order details: order id,line no,product id,quantity,unit price,discount,line sales amount,margin,discounted amount
8 orders: order id, order date,customer id, employee id,shipper id,freight
9 products: product id,product name,supplier id,category id,quantity per unit cost,unit price,unit in stock,units on order
10 shippment: order id,line no,shipper id,customer id,product id,employee id,shipment date
11 shippers: shipper id,company name
12 suppliers: supplier id,company name,contact name,address,city,postal code,country,phone,fax
13 yearly budget: year,target per year

These are the table: column name for the date provided to me 
we have to transform the data accordingly to make a power bi dashboard start with a preparing the data to transform to make a star schema.

Step 1: We create a facts table by merging order details,orders and shipments as we do not have a recieved order date and return date we use minimum shipment date of each order to compensate for the same
Step 2: We merge Products,Categories and Suppliers table on respective keys to form a merged table
Step 3 Customers and Divisions Table are merged
Step 4: employee,employees budget and offices are also merged.
Step 5: Create a Fiscal Date Table from April to March from the existing dates.
Step 6 : For units conversion a unit table is created.
Step 7: A dynamic selector for revenue and margin has been created to alter between the two for comprehensive analysis.
Step 8: Find various measures using dax and try visulaization to access meaningfull insights from the data.
