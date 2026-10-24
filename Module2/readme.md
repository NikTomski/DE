# SQL queries

1. Overview
  - Total Sales

```
SELECT SUM(sales) AS "Total Sales"
FROM orders
```

![image](https://github.com/NikTomski/data-engineering/assets/142725457/8519b529-1ae6-4ae2-840b-8c208ab1cfe1)

  - Total Profit

```
SELECT SUM(profit) AS "Total Profit"
FROM orders
```

![image](https://github.com/NikTomski/data-engineering/assets/142725457/7b76610e-2256-477a-bbc5-bb3e94c401d5)

  - Profit Ratio

```
SELECT profit/sales*100 AS "Profit Ratio"
FROM orders
```

![image](https://github.com/NikTomski/data-engineering/assets/142725457/a6edf603-433d-419d-bb8d-bb9bc5631d22)

  - Profit per Order

```
SELECT order_id, profit
FROM orders
```

![image](https://github.com/NikTomski/data-engineering/assets/142725457/571e6f59-82fc-4c02-a6f3-0e306f9a3591)

  - Sales per Customer

```
SELECT customer_id, sales 
FROM orders
```

![image](https://github.com/NikTomski/data-engineering/assets/142725457/7bb24b86-ef85-4778-a716-51748154bc4e)

  - Avg. Discount

```
SELECT AVG(discount)*100 as "Average Discount"
FROM orders
```

![image](https://github.com/NikTomski/data-engineering/assets/142725457/149d6c82-523e-4944-9185-7077c862527c)

  - Monthly Sales by Segment

```
SELECT EXTRACT(month from order_date) as month, segment, sales 
FROM orders
```

![image](https://github.com/NikTomski/data-engineering/assets/142725457/09dc514d-389b-4587-916a-f2338801c118)

  - Monthly Sales by Product Category

```
SELECT EXTRACT(month from order_date) as month, category, sales 
FROM orders
```

![image](https://github.com/NikTomski/data-engineering/assets/142725457/97b4c68c-adc6-4d50-be97-786e03857216)

 2. Product Dashboard
  - Sales by Product Category over time 

```
SELECT category, SUM(sales) 
FROM orders
GROUP BY category
```

![image](https://github.com/NikTomski/data-engineering/assets/142725457/7d486edc-ed21-4b8d-a321-fd4f4ff7b38f)

 3. Customer Analysis
  - Sales and Profit by Customer

```
SELECT customer_id, sales, profit
FROM orders
```

![image](https://github.com/NikTomski/data-engineering/assets/142725457/5adb3022-29be-439a-908f-31f3b52bcfc8)

  - Customer Ranking

```
SELECT customer_id, sales, profit
FROM orders
ORDER BY profit DESC, sales DESC
```

![image](https://github.com/NikTomski/data-engineering/assets/142725457/7c1eaa7a-e44e-40f0-a39e-edb73315f9ea)

  - Sales per region

```
SELECT region, SUM(sales)
FROM orders
GROUP BY region
```

![image](https://github.com/NikTomski/data-engineering/assets/142725457/a7ad65d7-ccaa-4f8f-a557-6a4dbf86010e)

# Draw a Data Model in SQLdbm

Conceptual Data Model

![image](https://github.com/NikTomski/data-engineering/assets/142725457/4391a9aa-caeb-4c16-a6d5-e7c3a2573d4f)

Physical (Logical) Data Model 

![image](https://github.com/NikTomski/data-engineering/assets/142725457/42c11494-948f-4aa5-ba9d-d4590caced53)

# Dashboard in Google Looker Studio (https://lookerstudio.google.com/s/kO_RHeg4RJU)

![image](https://github.com/NikTomski/DE/assets/142725457/6007b5bf-84d7-4281-8a95-613299ed1016)

# Dashboard in Yandex DataLens (https://datalens.yandex/7m4jdxdtpip8w)

![image](https://github.com/NikTomski/data-engineering/assets/142725457/f85c2533-3eb4-423a-8943-09f942a7bda7)

