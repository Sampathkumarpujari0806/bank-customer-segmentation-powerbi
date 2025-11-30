# 🏦 Bank Customer Segmentation - Power BI Project
📘 Overview

This project focuses on analyzing and segmenting bank customers based on their demographics, transaction behavior, and account details using Power BI.
The goal is to identify loyal, new, and lost customers, uncover patterns in customer behavior, and provide data-driven insights to improve customer retention and marketing strategies.

---

# 🎯 Project Objectives
- To analyze customer demographics such as age, gender, and location to discover key customer groups.
- To segment customers based on transaction behavior and demographics for better understanding.
- To evaluate transaction behavior - volume, frequency, and amount over time.
- To identify high-value, loyal, and at-risk customers using RFM (Recency, Frequency, Monetary) analysis.
- To compare performance across customer segments based on revenue and activity.
- To identify high-value customers contributing most to profitability.
- To make data-driven decisions through clean, visual, and dynamic dashboards.
- To give insights that help to improve customer retention and loyalty strategies.

---

# 🧩 Dataset Description
Dataset Name: bank_transactions.csv <br>
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

# 📊 Dashboard

## 1️⃣ Customer Demographics Analysis

<img width="1119" height="627" alt="Screenshot 2025-10-29 172108" src="https://github.com/user-attachments/assets/72ac078f-1f80-41ed-b53f-2b331cb53dd4" />

### 💡 Customer Demographics Insights
- Total Unique Customers are around 8,80,962.
- Average age of customers is  39 years .
- Total unique locations are 9298.
- Male customers make up 71.5% of the total, while female customers account for 28.5%, indicating that males are the majority.
- The 36–45 age group has the highest number of customers (around 4,11,610).Among males, the 46–55 age group has the most customers (around 95,042).Among females, the 26–35 age group has the most customers (around 1,10,585).
- The top customer locations are Mumbai, followed by New Delhi, Bangalore, and Gurgaon. Based on the location data, most customers are from urban areas.
Bank should concentrate on improving Customer base in rural areas.

---

## 2️⃣ Transaction Overview 

<img width="1119" height="628" alt="Screenshot 2025-10-29 172206" src="https://github.com/user-attachments/assets/107b5f04-2c90-4e63-b14d-d87a38157026" />

### 💡 Transaction Overview Insights
- The total transaction volume is approximately 1.64 billion, with an average transaction amount of ₹1.57K.
- The maximum transaction amount recorded is ₹1.56 million, while the average account balance is ₹114.55K.
- The transaction volume decreased steadily from August 2016 to October 2016.
- The highest transaction volume was on 6th August (₹4,73,16,251), followed by 4th September (₹4,59,15,954).
- There was a 97% increase in transaction volume from 29th August to 4th September, followed by a drastic 84% decrease from 14th september to 23rd September.
- By October, the transaction volume had dropped significantly.
- Weekends in August and September had higher transaction volumes compared to weekdays.
- The peak transaction time is around 7 PM on Sundays, and on other days, most transactions also occur between 7 PM and 8 PM.
- Customers aged above 65 have the highest average transaction amount, while males aged 0–25 also record highest average transaction amounts.

---

## 3️⃣ Customer Segmentation 

<img width="1118" height="628" alt="Screenshot 2025-10-29 172346" src="https://github.com/user-attachments/assets/eac64543-037a-4770-b971-fb8b8909150e" />

<img width="1118" height="627" alt="Screenshot 2025-10-29 172506" src="https://github.com/user-attachments/assets/cb687fe1-aa0b-4720-88fc-79c535ceafeb" />

###  💡 Customer Segmentation Insights
- The dataset contains a total of 8,80,962 unique customers.
- Customers are segmented into three categories: Lost Customers are 8,06,955 ,Loyal Customers are 71,453, New Customers are 2,554.
- New Customers have the highest average revenue compared to Loyal and Lost Customers.
- Lost Customers contribute the highest total revenue and have made more transactions, followed by Loyal Customers, and then New Customers.
- Based on these insights, the bank should focus on re-engaging Lost Customers to increase overall profitability.
- The 36–45 age group has the largest number of customers, followed by the 26–35 age group.
- The bank should maintain its reputation among younger customers and understand the needs of other age groups to tailor services and improve engagement.
- The number of customers below 25 years is comparatively low.To attract this segment, the bank can introduce joint accounts for customers under 18 years along with their parents or guardians. This may encourage education loan adoption, benefiting both the bank and customers.
- In terms of RFM scores, Loyal and New Customers have higher scores compared to Lost Customers, indicating stronger engagement and recent activity.

---

# 🛠️ Tools & Technologies

| Tool                 | Purpose                                   |
| -------------------- | ----------------------------------------- |
| **Power BI Desktop** | Dashboard creation and data visualization |
| **Power Query**      | Data cleaning and transformation          |
| **DAX**              | Calculated measures                       |
| **Excel / CSV**      | Data source                               |
| **PowerPoint**       | Project presentation                      |

---

# 🚀 How to Use

 1.Download or clone this repository: <br>
    - https://github.com/Sampathkumarpujari0806/bank-Customer-Segmentation-powerbi.git<br>
 2.Open bank_customer_segmentation.pbix in Power BI Desktop.<br>
 3.Connect or refresh the dataset if needed.<br>
 4.Explore the dashboard and insights.

---
## 📊 Power BI File
The Power BI dashboard file (`.pbix`) is available below:

👉 [Download Bank Customer Segmentation Power BI File](https://drive.google.com/file/d/1ji6AZwu8tYMcDo_8HY32aauo2YN4zQfg/view?usp=sharing)

---

# 💼 Business Impact

- Helped the bank identify loyal, lost, and new customers for better customer management.
- Enabled targeted marketing and retention strategies to improve customer engagement.
- Provided data-driven insights to increase revenue and reduce customer churn.
- Supported better decision-making through clear visualization of customer and transaction trends.

---
# Conclusion

- The dashboard helps understand customer behavior and segments effectively.
- Lost customers form the largest group but still contribute major revenue.
- New customers have the highest average revenue per person.
- The analysis supports the bank in improving retention, loyalty, and profitability.
- Overall, the project provides a clear view of customer performance for better business decisions.

--- 
# 👤 Author & Contact

Author: Pujari Sampath Kumar <br>
🎓 B.Tech                   <br>
📧 Email: sampathkumarpujari4@gmail.com<br>
🔗 LinkedIn:http://www.linkedin.com/in/sampathkumarpujari<br>
💻 GitHub: https://github.com/Sampathkumarpujari0806



