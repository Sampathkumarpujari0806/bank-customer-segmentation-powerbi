# 🏦 Bank Customer Segmentation - Power BI Project
📘 Overview

This project focuses on analyzing and segmenting bank customers based on their demographics, transaction behavior, and account details using Power BI.
The goal is to identify loyal, new, and lost customers, uncover patterns in customer behavior, and provide data-driven insights to improve customer retention and marketing strategies.

---

# 🎯 Project Objectives
- To analyze customer demographics such as age, gender, and location to discover key customer groups.
- To segment customers based on transaction behavior and demographics for better understanding.
- To evaluate transaction behavior — volume, frequency, and amount over time.
- To identify high-value, loyal, and at-risk customers using RFM (Recency, Frequency, Monetary) analysis.
- To compare performance across customer segments based on revenue and activity.
- To identify high-value customers contributing most to profitability.
- To make data-driven decisions through clean, visual, and dynamic dashboards.
- To give insights that help to improve customer retention and loyalty strategies.

---

# 🧩 Dataset Description
Dataset Name: bank_transactions.csv
The Key columns of Dataset are:

| Column Name           | Description                                      |
|-----------------------|--------------------------------------------------|
| `TransactionID`       | Unique ID for each transaction                   |
| `CustomerID`          | Unique ID for each customer                      |
| `CustomerDOB`         | Date of birth of the customer                    |
| `CustGender`          | Gender of the customer                           |
| `CustLocation`        | City/location of the customer                    |
| `CustAccountBalance`  | Account balance at transaction time              |
| `TransactionDate`     | Date of transaction                              |
| `TransactionTime`     | Time of transaction                              |
| `TransactionAmount`   | Amount transacted (INR)                          |

---

# 🧠 Data Preparation (Power Query)

1.Imported dataset into Power BI <br>

2.Cleaned and transformed data:
 - Removed null values from CustomerDOB, CustGender, and CustomerLocation columns.
 - Filled null values in the CustAccountBalance column with ‘0’.
 - Converted data type (CustomerDOB from Text to Date,CustAccountBalance from Text to Decimal Number,TransactionDate from Text to Date,TransactionTime from Text to Time).
3. Added Columns :<br>
 - **Age**: Calculated based on the customer’s date of birth to understand their current age.<br>
 - **Day of the Week**: Extracted from the transaction date to identify which days have higher activity.<br>
 - **Hour of the Day**: Extracted from the transaction time to analyze peak transaction hours.<br>
 - **Age Group**: Categorized customers into groups (0-25,26-35,36-45,46-55,56-65,Above 65) for demographic analysis.<br>
 - **CustomerCategory**: Classified customers as Lost, New,and Loyal based on their recent transaction behavior and engagement frequency.<br>
 - **RMF Score**: A combined score based on Recency, Monetary, and Frequency metrics to evaluate customer value and loyalty.<br>
 - **RMF Category**: Segmented customers according to RMF score thresholds : ≤ 259 → Low, ≤407 → Medium, > 407 → High.

---





