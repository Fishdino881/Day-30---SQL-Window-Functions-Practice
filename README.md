# Day-30 SQL Window Functions Practice

Overview

On Day 30, I learned SQL window functions, which allow calculations across a set of rows related to the current row without collapsing results like GROUP BY.

---

Topics Covered

1. Window Functions (`OVER()`)

```sql
SELECT name, salary,
       AVG(salary) OVER() AS avg_salary
FROM employees;
```

Performs calculations across the entire result set.

---

2. PARTITION BY

Used to divide data into groups while keeping row-level details.

```sql
SELECT department, name, salary,
       AVG(salary) OVER(PARTITION BY department) AS dept_avg
FROM employees;
```

---

3. Common Window Functions

* `ROW_NUMBER()`
* `RANK()`
* `DENSE_RANK()`

```sql
SELECT name, salary,
       RANK() OVER(ORDER BY salary DESC) AS salary_rank
FROM employees;
```

---

SQL Practice

Applied window functions with real-style queries to improve accuracy and performance.

---

### Learning Outcome

* Understood difference between GROUP BY and window functions
* Learned ranking and running calculations
* Improved analytical SQL skills

---
