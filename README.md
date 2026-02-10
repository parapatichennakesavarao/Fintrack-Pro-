# 💰 FINTRACK PRO – CLI Finance Manager

FinTrack Pro is a **command-line based personal finance management system** developed using **Python, SQLite, and SQLAlchemy ORM**.  
It helps users manage daily expenses, analyze spending patterns, maintain monthly budgets, and store financial data persistently.

---

## 📌 Project Overview

Managing personal finances manually can be error-prone and time-consuming.  
**FinTrack Pro** solves this problem by providing a structured, database-driven CLI application that allows users to:

- Record daily expenses  
- Categorize spending  
- Track budgets  
- Generate analytics using SQL  

This project is **interview-oriented** and demonstrates real-world backend concepts.

---

## 🎯 Objectives

- Understand **ORM-based database interaction**
- Use **SQLite with Python**
- Implement **CRUD operations**
- Perform **analytics using raw SQL**
- Design a **modular CLI application**
- Build a **resume-worthy backend project**

---

## 🛠 Technologies Used

- **Python**
- **SQLite Database**
- **SQLAlchemy ORM**
- **Raw SQL Queries**
- **Command Line Interface (CLI)**

---

## ⚙️ System Features

- ➕ Add Expense  
- ✏️ Update Expense  
- ❌ Delete Expense  
- 🔍 Search Expenses by Date  
- 📊 Category-wise Analytics  
- 🚨 Monthly Budget Alert  
- 💾 Persistent Storage using SQLite  

---

## 🗄 Database Design

### Tables

| Table Name | Columns |
|----------|--------|
| `categories` | id, name |
| `expenses` | id, title, amount, date, category_id |
| `subscriptions` | id, name, amount, next_date |
| `budgets` | id, month, limit |

### Relationships
Category 1 -------- N Expenses 

Each category can have multiple expenses (One-to-Many relationship).

---

## 🧩 Modules Description

### 1️⃣ Expense Module
- Add new expenses
- Update existing expenses
- Delete expenses
- Uses **SQLAlchemy ORM** for database operations

### 2️⃣ Report / Analytics Module
- Category-wise total spending
- Aggregation using `GROUP BY`
- SQL joins between categories and expenses

### 3️⃣ Budget Module
- Set monthly budget limits
- Compare budget with total spending
- Alerts when budget exceeds limit

### 4️⃣ Search Module
- Search expenses by date
- Uses SQL filtering

---

## 🔄 Project Workflow

1. Application starts and displays a CLI menu  
2. User selects an operation (Add, Update, Delete, Search, Analytics, Budget)  
3. Input is taken from user  
4. SQLAlchemy ORM interacts with SQLite database  
5. Data is stored/retrieved persistently  
6. Results are displayed on the terminal  

---

## 📈 Sample SQL Used

'''sql
SELECT c.name, SUM(e.amount)
FROM categories c
JOIN expenses e
ON c.id = e.category_id
GROUP BY c.name;
---

## 🧠 Concepts Used

- Object Relational Mapping (ORM)
- CRUD Operations
- One-to-Many Relationships
- SQL Aggregation (`SUM`, `GROUP BY`)
- Raw SQL Execution
- Modular Programming
- CLI-based Application Design
- Database Persistence
- Python `datetime` Handling

---

## ✅ Why This Project Is Useful

- Helps users track personal expenses efficiently  
- Improves financial awareness and budgeting habits  
- Demonstrates real-world database-driven application development  
- Strong **backend + SQL** project for technical interviews  
- Easily extendable to **Flask / Django Web Applications**

---

## 🚀 Future Enhancements

- CSV / Excel Export  
- Flask or Django Web Interface  
- Authentication & User Accounts  
- Graphical Charts & Dashboards  
- Subscription Reminder Notifications  

---

## 🏁 Conclusion

FinTrack Pro demonstrates practical usage of **Python with databases**, combining **ORM, SQL, and CLI-based design** into a complete personal finance management system.  
It is well-suited for **academic submission**, **portfolio showcase**, and **technical interviews**.
