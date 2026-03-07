# Dataset Description

This project analyzes the relationship between **marketing campaigns, customer behavior, and sales performance** using a simulated e-commerce dataset.

The dataset contains four tables representing different aspects of the business:

* customers
* products
* orders
* campaigns

Each dataset contains **500 records** and can be joined using primary and foreign keys.

> Note: This dataset is **not real**. The data was generated with the help of **Artificial Intelligence (ChatGPT)** and structured/assembled by me for educational and portfolio purposes.


# Data Model

The dataset follows a simple relational structure:

```
Customers (1) → (Many) Orders
Products  (1) → (Many) Orders
Campaigns → Marketing performance data
```

Orders act as the **central transactional table** connecting customers and products.


# Tables Overview

## 1. Customers

Contains information about registered customers.

| Column           | Description                         |
| ---------------- | ----------------------------------- |
| customer_id      | Unique identifier for each customer |
| first_name       | Customer first name                 |
| last_name        | Customer last name                  |
| email            | Customer email address              |
| country          | Country of the customer             |
| city             | Customer city                       |
| signup_date      | Date when the customer registered   |
| customer_segment | Customer type (New, Returning, VIP) |

**Primary Key**

```
customer_id
```


## 2. Products

Contains information about products available for sale.

| Column         | Description               |
| -------------- | ------------------------- |
| product_id     | Unique product identifier |
| product_name   | Name of the product       |
| category       | Product category          |
| price          | Selling price             |
| cost           | Product cost              |
| stock_quantity | Available stock           |
| supplier       | Product supplier          |

**Primary Key**

```
product_id
```


## 3. Orders

Represents purchase transactions made by customers.

| Column         | Description                                               |
| -------------- | --------------------------------------------------------- |
| order_id       | Unique order identifier                                   |
| customer_id    | ID of the customer who placed the order                   |
| product_id     | Purchased product                                         |
| order_date     | Date of the order                                         |
| quantity       | Number of items purchased                                 |
| order_status   | Order status (Completed, Cancelled, Returned, Processing) |
| payment_method | Payment type                                              |
| total_price    | Total order value                                         |

**Primary Key**

```
order_id
```

**Foreign Keys**

```
customer_id → customers.customer_id
product_id → products.product_id
```


## 4. Campaigns

Contains marketing campaign performance metrics.

| Column        | Description                                                                |
| ------------- | -------------------------------------------------------------------------- |
| campaign_id   | Unique campaign identifier                                                 |
| campaign_name | Campaign name                                                              |
| campaign_type | Marketing channel (Email, Social Media, Google Ads, Influencer, Affiliate) |
| start_date    | Campaign start date                                                        |
| end_date      | Campaign end date                                                          |
| budget        | Campaign budget                                                            |
| clicks        | Number of clicks                                                           |
| conversions   | Number of conversions                                                      |


# Dataset Characteristics

* **Synthetic dataset generated for analytical practice**
* **500 records per table**
* Designed for practicing:

  * SQL joins
  * business analytics
  * marketing performance analysis
  * customer behavior analysis
  * dashboard creation


# Possible Analytical Use Cases

This dataset allows analysis such as:

* marketing campaign performance
* customer segmentation
* revenue by product category
* sales trends over time
* customer acquisition patterns
* product profitability analysis
