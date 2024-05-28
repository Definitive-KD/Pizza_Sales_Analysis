# Pizza_Sales_Analysis

# Pizza Sales Insights-Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/6deac261-4d13-43b9-8c05-4fa49f2668e1/d3e1ddccb001ee31e3ea?experience=power-bi

## Problem Statement

This dashboard empowers pizzeria managers to understand their pizza sales and identify areas for improvement.
-	Customer Preferences: Analyze which pizzas are most popular and least popular, allowing you to tailor your menu to better suit customer tastes.
-	Sales Performance: Track sales trends over time to identify peak hours, days, or weeks. This helps with inventory management and staffing decisions.

  
By leveraging these insights, pizzeria managers can make data-driven decisions to:
-	Boost Sales: Promote popular pizzas and develop targeted marketing campaigns.
-	Reduce Costs: Optimize inventory and identify areas to streamline operations.

This dashboard is a valuable tool for any pizzeria manager looking to gain a deeper understanding of their business and make data-driven decisions for success.





### KPI's REQUIREMENT

We need to analyze key indicators for our pizza sales data to gain insights into our business performance. Specifically, we want to calculate the following metrics:

-	Total Revenue: The sum of the total price of all pizza orders.
-	Average Order Value: The average amount spent per order, calculated by dividing the total revenue by the total number of orders.
-	Total Pizzas Sold: The sum of the quantities of all pizzas sold.
-	Total Orders: The total number of orders placed.
-	Average Pizzas Per Order: The average number of pizzas sold per order, calculated by
-	dividing the total number of pizzas sold by the total number of orders.


### CHARTS REQUIREMENT

We would like to visualize various aspects of our pizza sales data to gain insights and understand key trends. We have identified the following requirements for creating charts:

-	Daily Trend for Total Orders: Create a bar chart that displays the daily trend of total orders over a specific time period. This chart will help us identify any patterns or fluctuations in order volumes on a daily basis.

-	Monthly Trend for Total Orders: Create a line chart that illustrates the hourly trend of total orders throughout the day. This chart will allow us to identify peak hours or periods of high order activity.

-	Percentage of Sales by Pizza Category: Create a pie chart that shows the distribution of sales across different pizza categories. This chart will provide insights into the popularity of various pizza categories and their contribution to overall sales.

-	Percentage of Sales by Pizza Size: Generate a pie chart that represents the percentage of sales attributed to different pizza sizes. This chart will help us understand customer preferences for pizza sizes and their impact on sales.

-	Total Pizzas Sold by Pizza Category: Create a funnel chart that presents the total number of pizzas sold for each pizza category. This chart will allow us to compare the sales performance of different pizza categories. 

-	Top 5 Best Sellers by Revenue, Total Quantity and Total Orders: Create a bar chart highlighting the top 5 best-selling pizzas based on the Revenue, Total Quantity, Total Orders. This chart will help us identify the most popular pizza options.

-	Bottom 5 Best Sellers by Revenue, Total Quantity and Total Orders: Create a bar chart showcasing the bottom 5 worst-selling pizzas based on the Revenue, Total Quantity, Total Orders. This chart will enable us to identify underperforming or less popular pizza options.

### Softwares Used

        MS OFFICE/ EXCEL: VERSION 2021
        MS SQL SERVER: 20.0
        SQL SERVER MANAGEMENT STUDIO - 2022 (RTM) - 16.0.1000.6
        POWER BI: MAY 2024 Version



### Steps followed 

- Step 1 : Create a Pizza database in SQL Server and import data in MS SQL Server.
- Step 2: Write SQL queries to get the data based on the problem statement and KPI’s requirements.
- Step 3: Connect Power BI to SQL server and import data into Power BI Desktop.
- Step 4: Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 5: Also, since by default, profile will be opened only for 1000 rows, so you need to select "column profiling based on entire dataset".
- Step 6 : It was observed that in none of the columns errors & empty values were present.
- Step 7 : “pizza_size” column was transformed. [S,M,L,XL] >> [Small, Medium, Large, X-Large]
- Step 7: dax written for new columns to be used in charts and formatting

        Order Day = UPPER(LEFT(pizza_sales[Day Name], 3))
        Order Month = UPPER(LEFT(pizza_sales[Month Name], 3))


- Step 9: Measures created to be used in charts and other measures

        Total Orders = DISTINCTCOUNT(pizza_sales[order_id])
        Total Pizzas Sold = SUM(pizza_sales[quantity])
        Total Revenue = SUM(pizza_sales[total_price])
        Avg Order Value = [Total Revenue] / [Total Orders]
        Avg Pizzas Per Order = [Total Pizzas Sold]/[Total Orders]

- Step 10:  Design the 2-page Power BI Dashboard. 

    Dashboard: Home Page

        Card visual added to display the below metrics.
        Total Revenue
        Average Order Value
        Total Pizzas Sold
        Total Orders
        Average Pizzas Per Order

        Daily trend for total orders (stacked column chart)
        Monthly Trend for total orders (area chart)
        Donut chart showing percentage of sales by Pizza category.
        Donut chart showing percentage of sales by Pizza size. 
        Funnel chart showing total pizza sold by Pizza category. 

        Pizza Category Slicer
        Time Interval Slicer
        Text Boxes for Analysis: Busiest Days & Times | Sales Performance
        Page Navigation Buttons



    Dashboard: Best/Worst Seller Page

        Stacked Bar Chart for Top 5 Pizzas by Revenue
        Stacked Bar Chart for Bottom 5 Pizzas by Revenue
        Stacked Bar Chart for Top 5 Pizzas by Quantity
        Stacked Bar Chart for Bottom 5 Pizzas by Quantity
        Stacked Bar Chart for Top 5 Pizzas by Orders
        Stacked Bar Chart for Bottom 5 Pizzas by Orders

        Text Box for Analysis :  Best Sellers | Worst Sellers
        Page Navigation Buttons
         
  
- Step 11: Two page report was created on Power BI Desktop & it was then published to Power BI Service.

![publish](https://github.com/Definitive-KD/Pizza_Sales_Analysis/assets/54216704/f4430724-ec34-416d-a704-18c08211c1e0)



### Following inferences can be drawn from the dashboard

        • Orders are highest on weekends, Friday/Saturday evenings.
        • There are maximum orders from the month of July and January.
        • Classic category contributes to maximum sales & total orders.
        • Large size pizza contributes to maximum sales.
        • The Thai Chicken Pizza Contributes to maximum Revenue.
        • The Classic Deluxe Pizza Contributes to maximum Total Quantities.
        • The Classic Deluxe Pizza Contributes to maximum Total Orders.
        • The Brie Carre Pizza Contributes to minimum Revenue.
        • The Brie Carre Pizza Contributes to minimum Total Quantities.
        • The Brie Carre Pizza Contributes to minimum Total Orders.

 

# Report Dashboard Snapshot: Home Page (Power BI Service)

![Dashboard-Home Pagge ](https://github.com/Definitive-KD/Pizza_Sales_Analysis/assets/54216704/8ce273dd-4e99-4ba3-b488-d089fe4365a3)

# Report Dashboard Snapshot: Best/Worst Seller Page  (Power BI Service)

![Dashboard - Best_Worst Seller Page](https://github.com/Definitive-KD/Pizza_Sales_Analysis/assets/54216704/7e8f1008-3de8-4bb3-9cd8-4c2c85e2ecff)
