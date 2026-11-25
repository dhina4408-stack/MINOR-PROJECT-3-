# MINOR-PROJECT-3-
A SQL-based fraud detection project analyzing 200K+ financial transactions using 12 fraud detection patterns in MySQL.
# 🚨 RedFlag – Fraud Detection Using SQL

## 📌 Project Overview

RedFlag is a SQL-based fraud detection project developed as part of The Unlox Academy – Data Analytics / Data Science Track (Week 3 Minor Project).

The project analyzes a synthetic financial transaction dataset from **PayFast**, a fictional Indian payment aggregator, to identify suspicious transaction patterns using MySQL.

The main objective is to detect potentially fraudulent activities by applying SQL queries, aggregations, filtering techniques, subqueries, Common Table Expressions (CTEs), and window functions.

## 🎯 Project Objectives

- Analyze large-scale financial transaction data.
- Identify suspicious transaction behaviors.
- Detect potential fraud using SQL queries.
- Understand transaction patterns across users and merchants.
- Generate insights that can support fraud investigation.

## 📂 Dataset Information

The project uses a synthetic transaction dataset containing approximately 200K+ transaction records.

| Attribute | Description |
|---|---|
| Dataset | RedFlag Fraud Detection |
| Payment Platform | PayFast (Fictional) |
| Records | 200,594 transactions |
| Observation Period | January – June 2024 |
| Users | 14,755 |
| Merchants | 800 |
| Database | MySQL |

### Dataset Columns

- `txn_id` – Unique transaction ID
- `user_id` – Customer ID
- `merchant_id` – Merchant ID
- `amount` – Transaction amount
- `txn_time` – Transaction date and time
- `status` – Transaction status (SUCCESS / FAILED)
- `payment_mode` – Payment method
- `city` – Transaction location
- `txn_type` – Transaction type (DEBIT / CREDIT / REFUND)

## 🔍 12 Fraud Detection Patterns

The project investigates the following suspicious activities:

1. **Velocity Fraud** – Detecting users making an unusually high number of transactions within a single day.

2. **Round Amount Clustering** – Identifying repeated transactions involving specific round amounts.

3. **Card Testing** – Detecting multiple low-value transactions below ₹10.

4. **Failed-Then-Succeeded Transactions** – Identifying repeated failed transactions followed by successful transactions of the same amount.

5. **Odd-Hour Concentration** – Detecting unusual transaction activity during early morning hours (02:00–04:59).

6. **Mule Accounts** – Identifying suspicious credit and debit transaction patterns within a short time interval.

7. **Refund Abuse** – Detecting users with unusually high refund transaction ratios.

8. **Merchant Collusion** – Identifying merchants where a small group of users contributes a disproportionately high transaction value.

9. **Structuring / Threshold Avoidance** – Detecting repeated transactions of exactly ₹9,999.

10. **Dormant-Then-Active Accounts** – Identifying accounts that become active after a long period of inactivity.

11. **Velocity Spike** – Detecting unusual increases in monthly transaction activity.

12. **Geographic Impossibility** – Identifying transactions occurring in different cities within a short time interval.

## 🛠️ Tools & Technologies

- MySQL
- MySQL Workbench
- SQL
- Data Analysis
- Fraud Pattern Detection

## 📊 SQL Concepts Used

- SELECT statements
- WHERE and HAVING clauses
- GROUP BY and ORDER BY
- Aggregate Functions (COUNT, SUM, AVG, MAX)
- Subqueries
- EXISTS
- Common Table Expressions (CTEs)
- Window Functions (LAG, ROW_NUMBER)
- CASE Statements
- Date and Time Functions
- Joins

## 📁 Project Structure

```text
RedFlag-Fraud-Detection/
│
├── README.md
│
├── redflag_transactions.sql
│
├── RedFlag_Fraud_Detection.sql
│
└── RedFlag_Project_Completed.pdf
```

## ⚙️ How to Run the Project

1. Install MySQL and MySQL Workbench.
2. Download or clone this repository.
3. Open `redflag_transactions.sql` in MySQL Workbench.
4. Execute the SQL script to create the database and import the transaction data.
5. Verify the imported records:

```sql
SELECT COUNT(*)
FROM redflag.transactions;
```

6. Open `RedFlag_Fraud_Detection.sql`.
7. Execute the queries individually or as a script.
8. Review the results to identify suspicious transaction patterns.

## 📈 Project Outcomes

The project applies 12 SQL-based fraud detection techniques to identify suspicious users, merchants, and transaction behaviors.

The analysis demonstrates how SQL can be used to:

- Identify abnormal transaction frequencies.
- Detect suspicious payment activities.
- Analyze user and merchant behavior.
- Identify potential refund and transaction manipulation.
- Support data-driven fraud investigation.

**Note:** Pattern 11 produces 66 matches under the implemented six-month average definition, compared with the 35–45 expected in the project brief. This difference is documented for validation.

## ⚠️ Disclaimer

This project uses synthetic transaction data and a fictional payment platform. The detected patterns are indicators for further investigation and do not independently establish fraudulent activity.

## 👨‍💻 Author

**Data Analytics / Data Science Student**

Project: RedFlag – Fraud Detection Using SQL

Learning through practical data analysis and SQL-based problem solving.

---

⭐ If you find this project interesting, feel free to explore the SQL queries and analysis!
