MIST 4610 - Project 1 - Group 7:

## Team Name:

- 61608 Group 7
## Team Members:

- Allmond, Chandler [@Chandler Allmond](https://github.com/chandlerallmond)
- Barton, Nick [@Nick Barton](https://github.com/nicholasbarton1)
- Manav Kamdar [@Manav Kamdar](https://github.com/manavk2004)
- Sengaphone, Vincent [@Vincent Sengaphone](https://github.com/sengaphone)
- Wilson, Landon [@Landon Wilson](https://github.com/landonnn0)

## Problem Description:
Retail technology businesses, such as Best Buy, face challenges in efficiently managing inventory, sales transactions, and product categorization. Without an organized database system, these businesses may encounter difficulties such as:

- Overstocking or understocking due to poor inventory tracking.
- Inefficient sales tracking, leading to unclear insights on employee performance and product demand.
- Difficulty in categorizing products, which slows down retrieval and impacts customer service.
- Lack of visibility into sales trends, making it harder for management to optimize stock levels and pricing strategies.
To address these challenges, the Electronic Product Database is designed as a comprehensive inventory and sales tracking system. This database will:

- Store detailed product information, including descriptions, pricing, warranty periods, and brand associations.
- Track real-time inventory status, restock dates, and reorder quantities.
- Facilitate sales transactions, recording employee sales contributions, transaction amounts, and payment methods.
- Enable sales analysis, allowing management to identify top-selling products, evaluate employee performance, and forecast future demand. 
By implementing this database, businesses can improve inventory accuracy, sales efficiency, and data-driven decision-making to enhance overall operations.
## Data Model:
The Electronic Product Database is designed to manage the inventory and sales of an electronics retail business. This data model provides a structured way to store and retrieve information about electronic products, their availability, and their categorization. The electronic_product table serves as the core of the model, linking products to their respective brands and categories through the brand_name and type_of_device tables. Additionally, the inventory table ensures that stock levels and restocking requirements are efficiently tracked, preventing shortages and optimizing supply chain operations.

The sales transaction process is handled through the sales_transaction and sales_transaction_product tables, which record transaction details, payment methods, and the number of products sold. Each sale is associated with an employee, stored in the employee table, allowing management to track individual employee contributions to sales. This structure ensures that every transaction is linked to both the products being sold and the employees processing the sales, making it easier to evaluate performance and analyze revenue trends.

By integrating inventory, sales, and employee management, this database provides businesses with real-time insights into product performance, stock availability, and financial transactions. The structured relationships between tables allow for streamlined data retrieval, enabling managers to make data-driven decisions regarding restocking, sales strategies, and employee performance evaluations. This system ultimately helps improve operational efficiency, profitability, and customer satisfaction by ensuring that products are always available and transactions are accurately recorded.

<img width="930" alt="422441874-fd30e664-1276-4929-ad69-98a52e26c572" src="https://github.com/user-attachments/assets/8768ee17-8cb9-451e-8900-9cd2addd711a" />

## Data Dictionary:
<img width="920" alt="422442581-1c8b02df-ea89-462f-a8c7-c347bd8bb99c" src="https://github.com/user-attachments/assets/c350616f-4a63-454f-8a18-366ca844efcb" />
<img width="920" alt="422442793-196067c9-c487-4d52-a7e7-5e63b3deb49e" src="https://github.com/user-attachments/assets/3c746ea2-d271-455c-8166-beb5ec261957" />
<img width="923" alt="422443018-d2aba09a-718f-4ed5-81c6-2361936d80d5" src="https://github.com/user-attachments/assets/232c103d-58b1-4f3a-8e7a-c7336c1eba6f" />
<img width="923" a<img width="919" alt="422443182-90e710fc-a6a0-4faa-944d-d0d2d779908e" src="https://github.com/user-attachments/assets/80b11e60-0562-4f11-b045-c54d62f7a2c2" />
<img width="922" alt="422443423-4ee88f02-8aea-48d8-b4ad-1d6a984d4713" src="https://github.com/user-attachments/assets/571caf20-588d-488f-a5f3-f22bea43dd57" />
<img width="923" alt="422443560-d5afeb49-4003-46a0-a751-ebdf3b549c6b" src="https://github.com/user-attachments/assets/5b31630f-ca22-4459-895e-3e03403e2939" />
<img width="925" alt="422443686-53edb716-5441-4c87-875b-ad372fb2bc76" src="https://github.com/user-attachments/assets/01f025a2-7835-46ed-99c6-616944934f43" />


## Queries:
1. Low Stock & High Stock Alert This query identifies products with low stock levels and high stock levels to help businesses manage inventory efficiently. The low stock alert retrieves products with a stock quantity of 30 or less, ensuring that managers restock them before they run out. The high stock alert retrieves products with a stock quantity greater than 50, helping managers avoid excessive inventory that could lead to high storage costs or markdowns. Both queries order the results in ascending order of stock quantity for better visibility.
<img width="940" alt="422444449-9825fb50-3228-4f51-ac76-0a7f42b22c4a" src="https://github.com/user-attachments/assets/6fc8ac15-bb1b-43dd-954d-b3d07a275aac" />

Managers can use this query to maintain balanced stock levels by ensuring that fast-selling products are restocked in time while preventing overstocking of slow-moving items. This helps businesses reduce waste, improve cash flow, and optimize inventory space, leading to better profitability and operational efficiency.


2. Best Selling Products This query retrieves the top 5 best-selling products based on the total quantity sold. The results are sorted in descending order by sales volume.
<img width="940" alt="422445095-a70d252a-a1b5-4138-991b-bebf90b33eee" src="https://github.com/user-attachments/assets/209ab894-db9d-487f-851d-43fe31844d28" />

Managers can identify high-demand products, allowing them to prioritize restocking and promotional efforts.

3. Total Revenue By Product Category This query calculates the total sales revenue for each product category while filtering out categories that generate less than the average revenue of all categories. It first groups transactions by product category to compute total revenue and then applies a HAVING clause to retain only those categories that exceed the average revenue. A subquery is used to determine the overall average category revenue, ensuring that the analysis focuses on high-performing product categories.

<img width="940" alt="422452611-346ad81c-0651-4170-bef2-df8ba2ae3542" src="https://github.com/user-attachments/assets/bc722e62-4f70-4195-a7b2-5de68d6434f0" />

Managers can use this query to identify high-performing product categories that generate above-average revenue. By filtering out lower-performing categories, businesses can allocate more resources to profitable categories, optimize inventory planning, and adjust marketing strategies for better financial outcomes.

4. Top 3 Most Profitable Brands If a store wanted to maximize revenue by stocking the brands from which consumers were purchasing most from, this code would be beneficial to visualize which brands sat at the top of the revenue chart.
<img width="940" alt="422445403-85e5a732-629e-4bcb-be0c-ebb76f3cb26f" src="https://github.com/user-attachments/assets/b39e7a76-96f7-48b9-bf96-d63f3d98ba0e" />

The code joins the sales transaction, sales transaction for products, electronic product, and brand name tables then groups it by brand name then order by total revenue. Then we set the limit to 3 in order to show only the top 3 brands by revenue.

5. Employee Preformance Shows each of the employee’s sales performance and gives basic information including their name and employee id
<img width="940" alt="422445574-34a14eab-c2d0-4500-8977-781249cee2f1" src="https://github.com/user-attachments/assets/c6f614bf-36f7-4f10-9eae-3b38eca5c2a4" />

Managers can use this to gauge whether employees are meeting the standards that the company has set for itself. Having a clear and concise table showing the level of performance each employee brings into the company can allow managers to pinpoint those who may need extra assistance, and give the proper guidance for success. Comparing the performance of each employee overtime can allow the managers to make logical decisions to keep employees, fire employees, give bonuses, etc.

6. Monthly Sales Trends This query displays the year, month, and total sales revenue for each month. The results are grouped by month and sorted in descending order to show the most recent months first.
<img width="940" alt="422445726-0e9249d5-c9d2-4f36-8515-767167509958" src="https://github.com/user-attachments/assets/4411dd30-a91a-40f7-8d6d-088b9be3cbfc" />
Managers can use this query to analyze sales trends over time, identifying seasonal patterns and peak sales months. This insight helps businesses make data-driven decisions about inventory management, pricing strategies, and marketing campaigns to maximize revenue.

7. Total Sales Transactions This query retrieves the total number of transactions in the system.
<img width="940" alt="422445856-a6e407a2-d051-4a28-8ffc-964a32515420" src="https://github.com/user-attachments/assets/aed35c61-2cff-4c9f-8c7e-31fe0cac8a44" />

Gives managers a quick snapshot of overall sales activity.

8. List of All Employees Retrieves basic employee details, sorted alphabetically by last name.
<img width="940" alt="422445991-731cd665-8777-4b40-ac30-a1f78fe89ddc" src="https://github.com/user-attachments/assets/b2cc89de-ca7c-44a5-9896-abcd7245db1b" />

Provides a quick reference for employee records.

9. Most Used Payment Method Finds the most frequently used payment methods.

<img width="940" alt="422446174-e814dd2b-a3da-416e-9576-644b6c67af11" src="https://github.com/user-attachments/assets/05f1b798-5064-41c5-ac7c-a5353d56c765" />

Helps managers analyze customer payment preferences.

10. Average TransactionValue Shows the average transaction value of each customer, meaning the average amount that a customer will spend.

<img width="945" alt="422446287-b70ac001-0352-436d-95d7-8c7f9afd8c25" src="https://github.com/user-attachments/assets/e274716c-7422-42ed-8625-cd56683d4c89" />

While this code is quite simple, managers can use this in a variety of ways. Taking a sample set of a few months and using it as a barometer for the following months can allow managers to see if there are fluctuations in the amount that customers usually spend. If significant fluctuations occur during certain parts of the year, managers can conclude that their product/service may have a seasonality component to it. If suddenly consumers start spending less, there may be new competition that has entered the market that the manager may be unaware of. If consumers are buying a lot of product, but there’s a disconnect with the transaction value, the product simply may not be priced high enough


## Database Information:

<img width="940" alt="422511206-a40065e9-4fc9-4906-a58f-c560c4a51eca" src="https://github.com/user-attachments/assets/bdcf124d-a60f-4732-b422-c6da723caf01" />

Name of the Database - ha_group7_crn61608

