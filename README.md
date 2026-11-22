# DBMS Lab – 25CSH-210

This repository contains my lab work for the **Database Management Systems (DBMS)** course (**25CSH-210**). It covers 10 experiments, from ER diagram design and schema creation to SQL querying, views, stored procedures, triggers, normalization, transactions, indexing and query optimization.

All SQL is written for **MySQL 8.0+** (recursive CTEs, `CREATE OR REPLACE VIEW`, and InnoDB features are used).

---

## 👤 Student Details

| | |
|---|---|
| **Name** | Shivam Maurya |
| **UID** | 25LBCS3216 |
| **Section / Group** | _Section C |
| **Course** | Database Management Systems (25CSH-210) |

---

## 📚 Experiments Overview

| # | Experiment | Topics Covered | Files |
|---|-----------|----------------|-------|
| 1 | ER Diagram – Indian E-commerce Platform | Entities (Customer, Product, Order, OrderItem, Seller, Category, Payment, Delivery, Address), relationships, cardinality | `Experiment_1.pdf` |
| 2 | ER to Relational Schema | `CREATE TABLE`, Primary Keys, Foreign Keys, `NOT NULL`, `UNIQUE`, `ON DELETE CASCADE`, `ON DELETE SET NULL` | `Experiment_2.pdf` |
| 3 | Basic SQL Queries & Aggregates | `SELECT`, `WHERE`, `COUNT`, `AVG`, `MAX`, `MIN`, `SUM` on Employee / Department / Project tables | `Experiment_3/` |
| 4 | Joins & Subqueries | `JOIN`s, subqueries, `EXISTS`, simulated `INTERSECT` / `EXCEPT`, `GROUP BY`, `EXPLAIN` | `Experiment_4/` |
| 5 | Views & Recursive CTE | Department salary summary view, employee hierarchy view, view updatability, recursive CTE for reporting chains | `Experiment_5/` |
| 6 | Stored Procedures & Triggers | `transfer_employee` procedure, salary validation trigger, `Employee_Audit` logging, edge-case testing | `Experiment_6/` |
| 7 | Normalization | Functional dependencies, UNF → 1NF → 2NF → 3NF → BCNF, lossless join & dependency preservation | `Experiment_7/` |
| 8 | Transactions | `START TRANSACTION`, `COMMIT`, `ROLLBACK`, `SAVEPOINT`, isolation levels (BankingDB) | `Experiment_8/` |
| 9 | Indexing | Single-column & composite indexes on 5,000 railway booking records, before/after `EXPLAIN` comparison | `Experiment_9/` |
| 10 | Query Optimization | Slow-query analysis on `Sales_Analytics`, index usage, avoiding functions on filter columns, aggregation tuning | `Experiment_10/` |

---

## 📁 Repository Structure

```
DBMS_25CSH-210/
├── Certificates/
│   ├── Infosys-Certificate.pdf.pdf
│   └── sql_basic certificate.pdf
├── Experiment_1.pdf
├── Experiment_2.pdf
├── Experiment_3/
│   ├── Experiment_3.code          # DB + table creation and data insertion
│   ├── Experiment_3.Queries       # SQL queries only
│   └── Experiment_3.Ouput.csv     # Query outputs
├── Experiment_4/
│   ├── Experiment_4.Code
│   ├── Experiment_4.Queries
│   └── Experiment_4.Ouput.csv
├── Experiment_5/
│   ├── Experiment_5.code
│   └── Experiment_5.Queries
├── Experiment_6/
│   ├── Experiment_6.code
│   └── Experiment_6.Queries
├── Experiment_7/
│   ├── Experiment_7.code
│   └── Experiment_7.Queries.txt
├── Experiment_8/
│   ├── Experiment_8.code
│   └── Experiment_8.Queries.txt
├── Experiment_9/
│   ├── Experiment_9.code
│   └── Experiment_9.Queries.txt
├── Experiment_10/
│   ├── Experiment_10.code
│   └── Experiment_10.Queries.txt
└── README.md
```

**File naming convention**

- `*.code` – full script: creates the database, tables, inserts data, and defines any views/procedures/triggers.
- `*.Queries` / `*.Queries.txt` – only the queries to run after the setup script.
- `*.Ouput.csv` – recorded output of the queries (Experiments 3 and 4).

---

## ▶️ How to Run

1. Install **MySQL 8.0+** (and optionally MySQL Workbench).
2. Clone or download this repository:
   ```bash
   git clone https://github.com/<your-username>/DBMS_25CSH-210.git
   cd DBMS_25CSH-210
   ```
3. For any experiment, first run the setup script, then the queries:
   ```bash
   mysql -u root -p < Experiment_3/Experiment_3.code
   mysql -u root -p < Experiment_3/Experiment_3.Queries
   ```
   Or open the files in MySQL Workbench and execute them in order.
4. Experiments 5 and 6 reuse the database created in **Experiment 3** (`DBMS_Experiment3`), so run Experiment 3's setup first.

> Experiments 1 and 2 are handwritten reports in PDF form (ER diagram and schema design), so there is no SQL to execute for Experiment 1.

---

## 🛠️ Tools & Technologies

- MySQL 8.0 / MySQL Workbench
- SQL (DDL, DML, DCL/TCL)
- InnoDB storage engine

---

## 🏅 Certificates

The `Certificates/` folder contains my course-related certificates:

- Infosys certificate
- SQL (Basic) certificate

---

## 📝 Notes

- Sample data uses Indian names and realistic salary/department values for Employee, Department and Project tables.
- Experiment 9 and 10 use generated data (5,000 booking records via a recursive CTE) to make index benefits measurable with `EXPLAIN`.

---

## 📄 License

This repository is for academic/educational purposes.
