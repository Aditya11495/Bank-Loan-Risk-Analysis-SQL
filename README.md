🏦 Bank Loan Risk Analysis using SQL
📌 Project Overview

This project demonstrates a complete Bank Loan Risk Analysis System built using SQL.
It includes database creation, bulk data insertion, and analytical queries to extract business insights from loan and customer data.

The project simulates a real-world banking environment with:

100+ Customers

100 Credit History Records

50+ Loan Records

Risk Segmentation Queries

Business KPI Calculations

All SQL queries and outputs are documented in the attached PDF.


1️⃣
SELECT 
    ROUND(
        COUNT(CASE WHEN loan_status = 'Defaulted' THEN 1 END) * 100.0 
        / COUNT(*), 2
    ) AS default_rate_percentage
FROM Loans;

Business Insight:
Measures the percentage of total loans that resulted in default.
Helps assess overall credit risk exposure.

2️⃣ Average Loan Amount by Loan Type
SELECT 
    loan_type,
    ROUND(AVG(loan_amount),2) AS avg_loan_amount
FROM Loans
GROUP BY loan_type
ORDER BY avg_loan_amount DESC;

Business Insight:
Identifies which loan category has the highest average disbursement.

3️⃣ High-Risk Customers
SELECT 
    c.customer_id,
    c.name,
    ch.credit_score,
    ch.past_defaults
FROM Customers c
JOIN Credit_History ch 
ON c.customer_id = ch.customer_id
WHERE ch.credit_score < 600
   OR ch.past_defaults > 0
ORDER BY ch.credit_score ASC;

Business Insight:
Detects customers likely to default based on credit behavior.

