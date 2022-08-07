# restaurant_sales

In this project, I would be Performing EDA on a restaurant sales Dataset using SQL. The dataset was downloaded from Kaggle and imported into SQL Server Management Studio.

## DATA CLEANING

### The Date column (Separate date and order time from order_date column)

![restaurants_new_cols](https://user-images.githubusercontent.com/36451701/183313473-88ca8d87-0223-4308-9e54-527a80d8e13b.png)

### Checking for Null Values

## DATA JOINING

![restaurants_join](https://user-images.githubusercontent.com/36451701/183313091-8ab6338a-9e41-41e8-adaa-0e260c3b90ea.png)

![restaurants_join_b](https://user-images.githubusercontent.com/36451701/183313095-27f35de2-999a-4d97-ab95-d22d66f0e15c.png)

![restaurants_columns](https://user-images.githubusercontent.com/36451701/182049003-12629cad-14a5-4243-b493-e16fd4f20a81.png)


### Creating a CTE
In order to easily reference our joined table, I created a common table expression (CTE).

## BASIC CALCULATIONS USING AGGREGATE FUNCTIONS

1. What is the total amount of ordered?
2. What is the average total amount ordered?
3. What is the Total quantity of items sold?
4. What is the average delivery time?
5. What is the average rating for food?

![aggregate_functions_1](https://user-images.githubusercontent.com/36451701/183312672-2e0e3330-baf2-4b1e-86db-4f82a4be8823.png)

![aggregate_functions_2](https://user-images.githubusercontent.com/36451701/183312675-6f47a1c4-c8f0-4c85-b20b-d3add2a89a56.png)


### Snapshot of each zone

![aggregate_functions_zone_1](https://user-images.githubusercontent.com/36451701/182048654-b17569de-1841-447b-a985-051bd578e26b.png)

![aggregate_functions_zone_2](https://user-images.githubusercontent.com/36451701/182048678-7ab3170a-da69-424f-ac39-29cc30d5c542.png)

### Snapshot of each restaurant

![aggregate_functions_restaurant_1](https://user-images.githubusercontent.com/36451701/182049370-0407ecd8-9cd8-4a5b-9165-b66fff49ad4a.png)

![aggregate_functions_restaurant_2](https://user-images.githubusercontent.com/36451701/182049392-355447cd-87a5-4b85-8905-ca27b5f28f10.png)

1. Which restaurants had the most orders?

![aggregate_functions_restaurant_3](https://user-images.githubusercontent.com/36451701/182049478-0a3cbd51-afa8-425c-a453-b4dd8fe5a5f6.png)

![aggregate_functions_restaurant_4](https://user-images.githubusercontent.com/36451701/182049506-2c623be0-77d2-4f18-bcab-84f1bb2cf1b5.png)

2. Which restaurants had the highest customer rating?

![aggregate_functions_restaurant_ratingpng](https://user-images.githubusercontent.com/36451701/182049763-74b5dc4e-53b5-4312-be11-a20d446a8436.png)

![aggregate_functions_restaurant_rating2](https://user-images.githubusercontent.com/36451701/182049803-b0008e47-b70f-4179-bfdb-793a34a54704.png)

3. Which restaurants have the quickest delivery?

![aggregate_functions_delivery_time](https://user-images.githubusercontent.com/36451701/183312143-0e998d4d-1185-485c-a3bf-94f751f1fcb2.png)

![aggregate_functions_delivery_time_b](https://user-images.githubusercontent.com/36451701/183312185-30af36b9-7bf1-4d25-9618-798c89232da1.png)

4. What payment mode was used frequently by customers?

![aggregate_functions_payment_type](https://user-images.githubusercontent.com/36451701/183312551-1c6a6559-4471-4837-9428-e0d66847f633.png)

![aggregate_functions_payment_type_b](https://user-images.githubusercontent.com/36451701/183312552-e527fc3e-6a62-45da-9d97-a79f5877b74d.png)

5. What is the most liked cuisine?

![aggregate_functions_popular_cuisine](https://user-images.githubusercontent.com/36451701/183312935-6bc7cb6e-cd39-4450-9b00-8c5e0ef7806d.png)

![aggregate_functions_popular_cuisineb](https://user-images.githubusercontent.com/36451701/183312945-81d902eb-5591-4810-8d30-61f648fc9ceb.png)

## Summary

This project was for learning and practice purposes. I made use of various SQL statements such as the basic SELECT, WHERE AND FROM Statements, then I went a little more advanced by joining two tables together using the JOIN Statement. I created a CTE of the joined tables using sub-queries and combined it with other queries in order to extract insights from the data set.
