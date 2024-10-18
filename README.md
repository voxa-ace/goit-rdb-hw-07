# goit-rdb-hw-07

# Task 1

SELECT 
    id,
    YEAR(date) AS year,
    MONTH(date) AS month,
    DAY(date) AS day,
    date
FROM 
    orders_2;

# Task 2

SELECT 
    id,
    date AS original_date,
    DATE_ADD(date, INTERVAL 1 DAY) AS date_plus_one_day
FROM 
    orders_2;


# Task 3

SELECT 
    id,
    date AS original_date,
    UNIX_TIMESTAMP(date) AS timestamp_seconds
FROM 
    orders_2;


# Task 4

SELECT 
    COUNT(*) AS total_rows
FROM 
    orders_2
WHERE 
    date >= '1996-07-10 00:00:00' AND date < '1996-10-08 00:00:00';

# Task 5

SELECT 
    id,
    date,
    JSON_OBJECT('id', id, 'date', date) AS json_object
FROM 
    orders_2;
