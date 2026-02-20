Customer Shopping Behavior Analysis
📊 End-to-End Data Analytics Project (Python + SQL + Power BI)
Created by Nilesh Patil
________________________________________
📌 Project Overview
This project analyzes 3,900 customer transactions to uncover patterns in:
•	Customer demographics
•	Spending behavior
•	Product preferences
•	Subscription trends
•	Revenue distribution
The goal is to generate data-driven business insights that help improve revenue, customer engagement, and strategic decision-making.
________________________________________
📂 Dataset Summary
•	Total Records: 3,900
•	Total Columns: 18
•	Missing Values: 37 (Review Rating column)
🔎 Key Features
Customer Information
•	Customer ID
•	Age
•	Gender
•	Location
•	Subscription Status
Purchase Details
•	Item Purchased
•	Category
•	Purchase Amount (USD)
•	Season
•	Size
•	Color
Behavioral Data
•	Discount Applied
•	Promo Code Used
•	Previous Purchases
•	Frequency of Purchases
•	Review Rating
•	Shipping Type
________________________________________
🧹 Data Cleaning & Preprocessing (Python)
✔️ Data Inspection
df.head()
df.info()
df.describe(include='all')
df.isnull().sum()
✔️ Handling Missing Values
Filled missing values in Review Rating using category-wise median:
df['Review Rating'] = df.groupby('Category')['Review Rating'] \
    .transform(lambda x: x.fillna(x.median()))
✔️ Column Cleaning
•	Converted column names to lowercase
•	Replaced spaces with underscores
•	Made SQL-friendly
✔️ Feature Engineering
1️⃣ Age Segmentation
labels = ['young_adult','adult','middle_aged','senior']
df['age_group'] = pd.cut(df['age'], bins=4, labels=labels)
2️⃣ Purchase Frequency Mapping
Converted categorical frequency into numeric days.
________________________________________
✔️ Removing Redundant Columns
Confirmed promo_code_used was identical to discount_applied:
(df['discount_applied'] == df['promo_code_used']).all()
Removed duplicate column.
________________________________________
✔️ Export Cleaned Dataset
df.to_csv("customer_behavior.csv", index=False)
________________________________________
🗄️ Database Integration (PostgreSQL)
Connected Python to PostgreSQL using:
pip install psycopg2-binary sqlalchemy
Uploaded cleaned dataset into database table:
df.to_sql('customer', engine, if_exists='replace', index=False)
________________________________________
🧮 SQL Business Analysis
Performed structured analysis to answer key business questions.
________________________________________
📊 Revenue Analysis
Q1: Revenue by Gender
Q2: Revenue by Age Group
________________________________________
💰 Discount & Pricing Insights
Q3: Top 20 customers using discount but spending above average
Q4: Products with highest discount usage %
________________________________________
🛒 Product Performance
Q5: Top 5 products with highest average review rating
Q6: Top 3 most purchased products per category
________________________________________
🚚 Shipping & Purchase Behavior
Q7: Average purchase comparison (Standard vs Express shipping)
________________________________________
💳 Subscription & Customer Value
Q8: Do subscribed customers spend more?
Q9: Are repeat buyers more likely to subscribe?
________________________________________
👥 Customer Segmentation
Segmented customers into:
•	🆕 New (0 purchases)
•	🔁 Returning (1–5 purchases)
•	⭐ Loyal (>5 purchases)
________________________________________
📈 Power BI Dashboard
Built an interactive dashboard showing:
🔹 KPI Overview
•	Total Customers: 3.9K
•	Avg Purchase Amount: $59.76
•	Avg Review Rating: 3.75
________________________________________
🔹 Revenue by Category
•	Clothing – Highest Revenue (~100K+)
•	Accessories – Second
•	Footwear – Moderate
•	Outerwear – Lowest
________________________________________
🔹 Sales & Revenue by Age Group
•	Young Adults – Highest contribution
•	Middle Aged – Strong segment
•	Seniors – Slightly lower
________________________________________
🔹 Subscription Insights
•	73% Non-Subscribers
•	27% Subscribers
________________________________________
🔹 Interactive Filters
•	Subscription Status
•	Gender
•	Category
•	Shipping Type
________________________________________
💡 Key Business Insights
•	Clothing dominates both revenue and customer base.
•	Young Adults are the most valuable segment.
•	Subscription penetration is low (27%).
•	Outerwear category needs promotional strategy.
•	Customer rating suggests improvement opportunity.
________________________________________
🚀 Business Recommendations
✔ Promote subscription programs
✔ Improve product quality for better ratings
✔ Target young & middle-aged segments
✔ Offer category-based discounts
✔ Create loyalty programs for repeat buyers
________________________________________
🛠️ Tools & Technologies Used
•	🐍 Python (Pandas, NumPy)
•	🗄 PostgreSQL
•	🧮 SQL
•       📊 Power BI
•       📁 CSV Data Processing
________________________________________
📌 Project Workflow
1.	Data Collection
2.	Data Cleaning (Python)
3.	Feature Engineering
4.	Database Upload
5.	SQL Business Analysis
6.	Dashboard Visualization
7.	Business Insights & Recommendations
________________________________________
🎯 Conclusion
This project demonstrates:
•	End-to-end data analytics pipeline
•	Business-focused SQL analysis
•	Dashboard storytelling
•	Practical customer segmentation
It highlights how data-driven decisions can increase revenue and improve customer engagement.

