# 📊 goit-rdb-hw-03

![MySQL](https://img.shields.io/badge/MySQL-Workbench-blue)
![SQL](https://img.shields.io/badge/SQL-Basic-green)
![Status](https://img.shields.io/badge/status-completed-success)

---

## 📌 Overview

This project demonstrates fundamental SQL operations using **MySQL Workbench**.

It covers:
- Data selection  
- Aggregation  
- Filtering  
- Sorting  
- Grouping  

📂 **Schema:** `3 lesson`

---

## 🧩 Tasks & Solutions

---

### 🔹 1. Data Selection (SELECT)

📌 Select all columns from the `products` table:

```sql
🔹 1. 1 Вибірка даних (SELECT)
Вибрати всі стовпчики з таблиці products

SELECT * 
FROM products;

🔹 1. 2 Вибрати тільки стовпчики name, phone з таблиці shippers
SELECT name, phone
FROM shippers;
```

🔹 2. Агрегатні функції
Знайти середнє, максимальне та мінімальне значення ціни (price) у таблиці products:

```sql
SELECT 
    AVG(price) AS avg_price,
    MAX(price) AS max_price,
    MIN(price) AS min_price
FROM products;
```
🔹 3. Унікальні значення, сортування та обмеження
Обрати унікальні значення category_id та price,
відсортувати за спаданням ціни та вивести лише 10 рядків:

```sql
SELECT DISTINCT category_id, price
FROM products
ORDER BY price DESC
LIMIT 10;
```
🔹 4. Фільтрація даних
Знайти кількість продуктів у ціновому діапазоні від 20 до 100:

```sql
SELECT COUNT(*) AS product_count
FROM products
WHERE price BETWEEN 20 AND 100;
```

🔹 5. Групування даних
Знайти кількість продуктів та середню ціну для кожного постачальника (supplier_id):

```sql
SELECT 
    supplier_id,
    COUNT(*) AS product_count,
    AVG(price) AS avg_price
FROM products
GROUP BY supplier_id;
```


