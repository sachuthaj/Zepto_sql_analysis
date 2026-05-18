# Zepto_sql_analysis
Comprehensive SQL practice project on a custom employee-department database built with SQLite. Covers SELECT, WHERE, GROUP BY, HAVING, JOINs, subqueries, and window functions including RANK, PARTITION BY, and running totals.
# 🏢 Zepto SQL Analysis — End-to-End SQL Practice Project
> A comprehensive SQL analytics project built on a custom employee and department database, covering all core SQL concepts from basic queries to advanced window functions.

---

## 📌 Overview
This project demonstrates mastery of SQL by building a realistic employee and department database from scratch and executing 20+ business queries across all major SQL topics — filtering, aggregation, joins, subqueries, and window functions.

The project follows a complete SQL analytics pipeline:
```
SQLite Setup → Table Creation → Data Insertion → SQL Queries (Basic → Advanced) → Insights
```

---

## 📂 Dataset
**Source:** Custom-built synthetic dataset (100 employees, 20 departments)

### Employees Table
| Column | Description |
|--------|-------------|
| emp_id | Unique employee ID |
| emp_name | Employee full name |
| age | Employee age |
| gender | M / F |
| dept_id | Department ID (foreign key) |
| salary | Monthly salary (₹) |
| join_date | Date of joining |
| performance_score | Score out of 100 |
| email | Company email |

### Departments Table
| Column | Description |
|--------|-------------|
| dept_id | Unique department ID |
| dept_name | Department name |
| location | City (Bangalore, Mumbai, Delhi, etc.) |
| budget | Department budget (₹) |

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python | Environment setup and query execution |
| SQLite (sqlite3) | In-memory relational database |
| SQL | All querying and analysis |
| pandasql | SQL queries directly on DataFrames |
| Google Colab | Development environment |
| GitHub | Version control and project sharing |

---

## 🔢 SQL Concepts Covered

### Basic Queries
```sql
SELECT, WHERE, BETWEEN, LIKE, IS NULL, IS NOT NULL, LIMIT
```

### Aggregations
```sql
COUNT, SUM, MAX, MIN, AVG, ROUND
```

### Grouping & Filtering
```sql
GROUP BY, HAVING, ORDER BY
```

### Joins
```sql
INNER JOIN, LEFT JOIN
```

### Subqueries
- Employees earning above average salary
- Highest earner per department

### Window Functions
```sql
RANK() OVER (ORDER BY salary DESC)
RANK() OVER (PARTITION BY dept_id ORDER BY salary DESC)
SUM() OVER (ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW)  -- Running Total
```

---

## 📋 Queries Run

| # | Query | Purpose |
|---|-------|---------|
| 1 | Filter by dept_id IN list | Employees in analytics/tech departments |
| 2 | Salary BETWEEN range | Mid-range salary employees |
| 3 | Join date filter | Employees who joined 2020–2021 |
| 4 | Name starts with 'A' | LIKE pattern matching |
| 5 | Email contains 'company' | Partial string search |
| 6 | IS NULL / IS NOT NULL | Missing salary check |
| 7 | COUNT total employees | Headcount |
| 8 | SUM / MAX / MIN / AVG salary | Salary statistics |
| 9 | AVG salary by dept | Department-wise pay analysis |
| 10 | Gender count | Workforce diversity |
| 11 | Dept avg salary > 80K | HAVING filter |
| 12 | Dept with > 5 employees | Headcount filter |
| 13 | INNER JOIN emp + dept | Employee with department name & location |
| 14 | LEFT JOIN | All employees including unassigned |
| 15 | Headcount + budget per dept | Department overview |
| 16 | Subquery — above avg salary | High earners |
| 17 | Subquery — max salary per dept | Top earner in each department |
| 18 | RANK() by salary | Overall salary ranking |
| 19 | PARTITION BY dept salary rank | Rank within each department |
| 20 | Running total of salary | Cumulative salary using window function |

---

## 📈 Key Results
- **Research and Analytics** departments have the highest average salaries
- Majority of high performers (score > 90) are concentrated in technical departments
- **Bangalore** has the highest number of employees across departments
- Running totals reveal how cumulative salary grows across the employee base

---

## 🚀 How to Run

**Prerequisites**
```
Python 3.x
pandas, sqlite3 (built-in), pandasql
Google Colab or Jupyter Notebook
```

**Steps**
1. Clone the repository
```bash
git clone https://github.com/your-username/zepto-sql-analysis.git
```
2. Open `zepto_analysis.ipynb` in Google Colab
3. No CSV upload needed — database is built inside the notebook
4. Run all cells sequentially (`Runtime → Run all`)

---

## 📁 Project Structure
```
zepto-sql-analysis/
│
├── notebook/
│   └── zepto_analysis.ipynb
│
└── README.md
```

---

## 👤 Author
**Sachutha**
B.Sc. Computer Science & Statistics — Kristu Jayanti College, Bengaluru
📧 sachuthaj@gmail.com · 🔗 LinkedIn · 💻 GitHub

---
> *Built as part of a data analytics portfolio to demonstrate end-to-end SQL skills — from basic filtering to advanced window functions — on a realistic employee dataset.*
