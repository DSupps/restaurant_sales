# restaurant_sales

In this project, I perfromed EDA on a restaurant sales Dataset using SQL. The dataset was downloaded from Kaggle and imported into SQL Server Management Studio.

Some of the questions I looked at answering:

1. What is the Total amount of orders?
2. What is the Total quantity of items sold?
3. What is the average delivery time?
4. What is the average rating for food?
5. What customer ordered the most?
6. What restaurant had the most orders?
7. What payment mode was used frequently by customers?
8. What is the most liked cuisine?
9. What time of the day did customers order the most?
10. What amount of customers did each zone have?
11. Which zone had the most orders

## DATA CLEANING

I want to create some summary statistics (mean, maximum, minimum values) to find some valuable insights from my dataset. In order to draw those accurate/valuable insights, I need my data to be accurate. First thing I did was check for any missing values.  Performing any statistical analysis on datasets without taking care of invalid entries may cause inaccurate analysis.

### Step 1) Check for Null Values

Confirm if my dataset had any null values.  Removing any null values so the performance and accuracy of the data are not adversely affected.

![data_cleansing_nulls](https://user-images.githubusercontent.com/36451701/188035081-16fc8d73-be6e-4e11-b277-3371aaa166cd.png)

No null vaues were found.

![data_cleansing_c](https://user-images.githubusercontent.com/36451701/188035205-04d7937c-8b4f-4995-ab26-fe2e17106adf.png)

### Step 2) Separate date and order time from "order_date" column.

The format of the order date column was Date/time. I extracted the time from it using the convert function since I would be needing it in my analysis.

![restaurants_new_cols](https://user-images.githubusercontent.com/36451701/183313473-88ca8d87-0223-4308-9e54-527a80d8e13b.png)

Create new columns "new_order_date" and "new_order_time" to analyze time performance. 

![data_cleansing](https://user-images.githubusercontent.com/36451701/188020268-bd6d94d4-3022-48ca-b089-1417c75fd1e4.png)


## DATA JOINING

### Creating a CTE

The first table "order" contains the order information while the second table "restuarants" contains the restaurant information. I will need the two tables merged in order to carry out my aggregate analysis.

In order to easily reference our joined table, I created a common table expression (CTE).

Using the join clause I was able to join the two tables together using the column specific to both tables.

![restaurants_join](https://user-images.githubusercontent.com/36451701/183313091-8ab6338a-9e41-41e8-adaa-0e260c3b90ea.png)

![restaurants_join_b](https://user-images.githubusercontent.com/36451701/183313095-27f35de2-999a-4d97-ab95-d22d66f0e15c.png)

![restaurants_columns](https://user-images.githubusercontent.com/36451701/182049003-12629cad-14a5-4243-b493-e16fd4f20a81.png)


## BASIC CALCULATIONS USING AGGREGATE FUNCTIONS

1. What zone had the most orders?
2. Which restuarants had the most orders?
3. Which restaurants had the highest customer rating?
4. Which restaurants have the quickest delivery time?
5. What payment mode was used frequently by customers?
6. What is the most popular cuisine?
7. What is the average total amount spent?
8. What is the total quantity of items sold?
9. What is the average delivery time?
10. What is the average rating for food?

![aggregate_functions_1](https://user-images.githubusercontent.com/36451701/183312672-2e0e3330-baf2-4b1e-86db-4f82a4be8823.png)

![aggregate_functions_2](https://user-images.githubusercontent.com/36451701/183312675-6f47a1c4-c8f0-4c85-b20b-d3add2a89a56.png)


### Question #1 - What zone had the most orders?

![aggregate_functions_zone_1](https://user-images.githubusercontent.com/36451701/182048654-b17569de-1841-447b-a985-051bd578e26b.png)

![aggregate_functions_zone_2](https://user-images.githubusercontent.com/36451701/182048678-7ab3170a-da69-424f-ac39-29cc30d5c542.png)

### Question #2 - Which restaurants had the most orders?

![aggregate_functions_restaurant_3](https://user-images.githubusercontent.com/36451701/182049478-0a3cbd51-afa8-425c-a453-b4dd8fe5a5f6.png)

![aggregate_functions_restaurant_4](https://user-images.githubusercontent.com/36451701/182049506-2c623be0-77d2-4f18-bcab-84f1bb2cf1b5.png)

### Question #3 - Which restaurants had the highest customer rating?

![aggregate_functions_restaurant_ratingpng](https://user-images.githubusercontent.com/36451701/182049763-74b5dc4e-53b5-4312-be11-a20d446a8436.png)

![aggregate_functions_restaurant_rating2](https://user-images.githubusercontent.com/36451701/182049803-b0008e47-b70f-4179-bfdb-793a34a54704.png)

### Question #4 - Which restaurants have the quickest delivery time?

![aggregate_functions_delivery_time](https://user-images.githubusercontent.com/36451701/183312143-0e998d4d-1185-485c-a3bf-94f751f1fcb2.png)

![aggregate_functions_delivery_time_b](https://user-images.githubusercontent.com/36451701/183312185-30af36b9-7bf1-4d25-9618-798c89232da1.png)

### Question #5 - What payment mode was used frequently by customers?

![aggregate_functions_payment_type](https://user-images.githubusercontent.com/36451701/183312551-1c6a6559-4471-4837-9428-e0d66847f633.png)

![aggregate_functions_payment_type_b](https://user-images.githubusercontent.com/36451701/183312552-e527fc3e-6a62-45da-9d97-a79f5877b74d.png)

### Question #6 - What is the most popular cuisine?

![aggregate_functions_popular_cuisine](https://user-images.githubusercontent.com/36451701/183312935-6bc7cb6e-cd39-4450-9b00-8c5e0ef7806d.png)

![aggregate_functions_popular_cuisineb](https://user-images.githubusercontent.com/36451701/183312945-81d902eb-5591-4810-8d30-61f648fc9ceb.png)

### Question #7 - What is the average total amount spent on an order?

![average_order_a](https://user-images.githubusercontent.com/36451701/189551038-4f8c2552-9471-4e79-943a-16d6ae502aea.png)

![average_order_b](https://user-images.githubusercontent.com/36451701/189551070-7166fb76-8123-4013-a98e-087979cc1b25.png)


### Question #8 - What is the total quantity of items sold?

![total_qty_sold_a](https://user-images.githubusercontent.com/36451701/189551223-6ad980e2-9cc7-498a-ad06-a50c93209941.png)

![total_qty_sold_b](https://user-images.githubusercontent.com/36451701/189554906-c2d9658f-12c5-4e53-95a8-1ed820309da1.png)

### Question #9 - What is the average delivery time?

![avg_delivery_time_a](https://user-images.githubusercontent.com/36451701/189554947-aa37726b-bdad-4eeb-85b1-9ec4d90220c4.png)

![avg_delivery_time_b](https://user-images.githubusercontent.com/36451701/189554991-ca21c52c-b804-4228-8f9d-399bd409a685.png)

### Question #10 - What is the average rating for food?

![food_rating](https://user-images.githubusercontent.com/36451701/189555224-78a734b0-81ee-44fa-8ff8-e40eb1e18ebf.png)

![aggregation_food_rating](https://user-images.githubusercontent.com/36451701/189555229-f9e19c67-2308-432a-a3ad-02b638e6d059.png)


## Summary

This project was for learning and practice purposes. I made use of various SQL statements such as the basic SELECT, WHERE AND FROM Statements, then I went a little more advanced by joining two tables together using the JOIN Statement. I created a CTE of the joined tables using sub-queries and combined it with other queries in order to extract insights from the data set.
