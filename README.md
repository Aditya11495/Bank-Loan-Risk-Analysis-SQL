**Project Overview**

This project simulates a real-world banking database to analyze loan risk, customer credit behavior, and approval trends using SQL.

The goal is to extract business insights such as:

Default Rate

High-Risk Customers

Credit Score Impact

Loan Approval Trends

Income vs Risk Relationship

City-wise Loan Distribution

Database Schema
Tables Used:

Customers

Loans

Credit_History

🧱 Table Structure
Customers

customer_id (Primary Key)

name

age

gender

income

employment_status

city

Loans

loan_id (Primary Key)

customer_id (Foreign Key)

loan_amount

loan_type

interest_rate

loan_term

loan_status (Approved / Rejected / Closed / Defaulted)
