# SQL & Relational Data — Notes

## What is SQL?

* **SQL (Structured Query Language)** is a language used for handling **structured, relational data**.
* SQL is mainly used with **RDBMS (Relational Database Management Systems)**.
* It helps users:

  * Store data
  * Retrieve data
  * Update data
  * Delete data
  * Manage relationships between tables

---

# Relational Database Concepts

## 1. Tables

A relational database stores information in **tables**.

Example tables from the slide:

* `Employees`
* `Departments`

Each table contains:

* **Fields (Columns)**
* **Records (Rows)**

---

## 2. Fields (Columns)

Fields represent the type of information stored in a table.

### Example: Employees Table Fields

| Field    | Description             |
| -------- | ----------------------- |
| `id`     | Unique employee ID      |
| `name`   | Employee name           |
| `salary` | Employee salary         |
| `dep_id` | Department ID reference |

### Example: Departments Table Fields

| Field      | Description          |
| ---------- | -------------------- |
| `id`       | Unique department ID |
| `dep_name` | Department name      |
| `location` | Department location  |

---

## 3. Records (Rows)

Records are individual entries inside a table.

### Example Records from Employees Table

| id | name  | salary | dep_id |
| -- | ----- | ------ | ------ |
| 1  | Max   | 10000  | 1      |
| 2  | Julie | 15000  | 1      |
| 3  | Marc  | 8000   | 3      |

### Example Records from Departments Table

| id | dep_name   | location |
| -- | ---------- | -------- |
| 1  | Developers | Munich   |
| 2  | Sales      | Berlin   |
| 3  | Accounting | Berlin   |

---

# Relationships in SQL

## Relations Between Tables

In relational databases, data is often split across multiple related tables.

The relationship is created using:

* **Primary Keys**
* **Foreign Keys**

### Example

* `Departments.id` → Primary Key
* `Employees.dep_id` → Foreign Key

This means:

* Employee records reference a department using `dep_id`.
* Multiple employees can belong to the same department.

---

# Database Normalization

## Normalized Data

Relational databases organize **normalized data** into multiple related tables.

Normalization helps:

* Reduce data duplication
* Improve consistency
* Make updates easier
* Organize data efficiently

---

# Important SQL Terminology

| Term           | Meaning                               |
| -------------- | ------------------------------------- |
| Table          | Collection of related data            |
| Row / Record   | Single data entry                     |
| Column / Field | Attribute of the data                 |
| Primary Key    | Unique identifier for records         |
| Foreign Key    | Field linking two tables              |
| Relation       | Connection between tables             |
| RDBMS          | Relational Database Management System |

---

# Key Takeaways

* SQL is used to manage relational databases.
* Data is stored in tables.
* Tables contain rows (records) and columns (fields).
* Relationships connect tables together.
* Normalization organizes data efficiently across multiple related tables.
* RDBMS systems use SQL to manage structured data.

---

# Example Relationship Visualization

```text
Employees.dep_id  --->  Departments.id
```

This connects employees to their departments.

