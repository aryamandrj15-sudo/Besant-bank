# BesantBank - MySQL Database System

A comprehensive relational database project for a banking system, covering the full lifecycle of data management—from schema design and data integrity to advanced automation using Triggers, Stored Procedures, and CTEs.

## 📌 Project Overview
BesantBank is designed to simulate core banking operations. The system manages customer account details and tracks financial transactions while maintaining real-time data accuracy through automated backend logic.

## 🚀 Key Features
* **Relational Schema:** Linked tables for `Accountdetails` and `Transactiondetails`.
* **Automated Accounting:** Uses **MySQL Triggers** to automatically update account balances when a Credit or Debit transaction occurs.
* **Business Logic:** Includes **Stored Procedures** for generating account mini-statements and checking account activity status.
* **Data Integrity:** Implements `CHECK` constraints (e.g., minimum age of 18) and `FOREIGN KEY` relationships to ensure data consistency.
* **Performance Optimization:** Includes indexing strategies for high-traffic columns.
* **Advanced Querying:** Demonstrates the use of **CTEs (Common Table Expressions)** and **Cursors** for row-by-row data processing.

## 📊 Database Schema

### `Accountdetails` Table
| Column | Type | Constraints |
| :--- | :--- | :--- |
| AccountID | INT | Primary Key |
| Name | CHAR(30) | NOT NULL |
| Age | TINYINT | CHECK (> 18) |
| Accounttype | VARCHAR(30) | Saving / Current |
| Currentbalance | INT | |
| AccountStatus | VARCHAR(20) | Active / Inactive |

### `Transactiondetails` Table
| Column | Type | Constraints |
| :--- | :--- | :--- |
| TransactionID | INT | PK, Auto-Increment |
| AccountID | INT | Foreign Key |
| Transactiontype | VARCHAR(10) | Credit / Debit |
| Transactionamount | INT | |
| Transactiontime | DATETIME | Default: NOW() |

