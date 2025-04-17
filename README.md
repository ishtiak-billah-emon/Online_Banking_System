# 🏦 Online Banking System - Oracle Database Project

<img src="./img/db.png" height ="400"
width="700"
title="oracle database">

Welcome to the **Online Banking System** project! This is a relational database management project built using **Oracle SQL** that simulates the backend structure of a mobile banking application named **ABC**. It includes a complete ER design, normalization process, relational schema, SQL queries and data manipulation examples.

## 📌 Project Description

**ABC Mobile Banking App** connects clients and banks to enable hassle-free financial transactions. It handles clients, accounts, loans, managers, employees, projects and payment gateways such as shopping, education and transport.

The aim is to develop a complete relational database with:
- Entity and relationship modeling
- Normalized schema
- SQL implementation using Oracle
- Advanced query examples including joins, subqueries and views

---

## 📊 ER Diagram Overview

The system is modeled with the following entities:
- **Bank**
- **Client**
- **Loan**
- **Manager**
- **Employee**
- **Project**
- **Payment**
- **Online Banking**

Relationships include:
- Clients can borrow loans
- Managers manage employees and organize projects
- Clients use multiple payment gateways
- Banks are managed by bank managers

---

## 🛠️ Database Design

### Entities

- **Bank**: `swift_code`, `bank_name`, `city`, `country`
- **Client**: `nid`, `first_name`, `last_name`, `dob`, `account_number`, `address`, `phone`
- **Loan**: `loan_no`, `amount`, `date`
- **Manager**: `m_id`, `name`, `address`, `salary`, `phone`
- **Employee**: `e_id`, `name`, `salary`, `phone`
- **Project**: `serial_no`, `project_name`, `project_date`
- **Payment**: `payment_slip_no`, `online_shopping`, `education_fee`, `transport_fee`
- **OnlineBanking**: Relationship table for clients and bank connections

---

## 📐 Normalization

The project goes through all stages of normalization:

- ✅ **1NF**: Atomic values ensured
- ✅ **2NF**: Partial dependencies removed
- ✅ **3NF**: Transitive dependencies removed

Each functional dependency is clearly documented and normalized accordingly.

---

## 🧱 Final Schema

| Table             | Key Fields |
|------------------|------------|
| `BANK`           | `swift_code` |
| `BANK_LOAN`      | `loan_no`, `swift_code` |
| `CLIENT`         | `account_number` |
| `CLIENT_LOAN`    | `c_nid`, `loan_no` |
| `CLIENT2`        | `c_nid` |
| `LOAN`           | `loan_no` |
| `EMPLOYEE`       | `e_id` |
| `MANAGER`        | `m_id` |
| `BANK_MANAGER`   | `m_id`, `swift_code` |
| `PROJECTS`       | `p_serial_no` |
| `PAYMENT`        | `payment_slip_no` |
| `ONLINE_BANKING` | `c_nid`, `swift_code` |
| `LOCATION`       | `city`, `country` |
| `JOINT_TABLE_2`  | For linking managers with contacts |

---

## 🧾 SQL Implementation

### ✅ Table Creation

All the necessary tables are created with appropriate **primary and foreign keys**, covering:
- Bank, Client, Loan
- Manager, Employee, Project
- Online banking relationships
- Payment gateway tracking

### 📥 Data Insertion

Sample data entries are included for:
- Banks
- Managers and Employees
- Clients and Loans
- Payment details
- Projects

---

## 🔍 Joins

- **Equi Join**: Get all bank info located in BARISHAL
- **Outer Join**: Show employees with or without a manager
- **Self Join**: Match payment values of online shopping & transport
- **Non-Equi Join**: [Query defined in script]

---
## 👤 Author

**Ishtiak Billah Emon**

📚  Oracle Database Project | B.Sc. in CSE  
🏫  American International University-Bangladesh (AIUB)


## 📌 Note

This project is built entirely for academic learning and demonstration purposes. It can be a great resource for understanding:
- Database design
- Real-world banking system modeling
- Writing optimized SQL queries

