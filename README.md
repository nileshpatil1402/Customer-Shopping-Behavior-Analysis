📊 Customer Shopping Behavior Analysis
End-to-End Data Analytics Project | Python • SQL • Power BI
This project analyzes transactional data from 3,900 purchases to uncover deep insights into customer spending patterns, demographics, and subscription behavior. The final goal is to provide data-driven recommendations for strategic business growth.
________________________________________
📌 Project Overview
The analysis tracks the customer journey from raw data to actionable business intelligence:
•	Demographics: Analysis by Age, Gender, and Location.
•	Product Performance: Revenue and popularity across categories like Clothing, Accessories, Footwear, and Outerwear.
•	Behavioral Trends: Impact of discounts, shipping types, and subscription status on total revenue.
________________________________________
🛠️ Tech Stack & Tools
•	Python: Data cleaning, feature engineering, and ETL.
•	PostgreSQL: Relational database storage and advanced business querying.
•	Power BI: Interactive dashboarding and KPI visualization.
________________________________________
📂 Dataset Summary
•	Total Records: 3,900 purchases.
•	Features: 18 columns including Customer ID, Age, Item Purchased, Purchase Amount, Review Rating, and Subscription Status.
•	Data Integrity: Handled 37 missing values in the Review Rating column using category-wise median imputation.
________________________________________
⚙️ Data Pipeline (Python & SQL)
1. Data Cleaning & Feature Engineering
•	Normalization: Converted column names to lowercase and replaced spaces with underscores for SQL compatibility.
•	Age Segmentation: Created groups: young_adult, adult, middle_aged, and senior.
•	Frequency Mapping: Converted categorical purchase frequencies (e.g., "Fortnightly") into numeric days (e.g., 14) for quantitative analysis.
•	Redundancy Removal: Dropped promo_code_used after confirming it was identical to discount_applied.
2. Database Integration
Connected Python to PostgreSQL using sqlalchemy and uploaded the cleaned dataset for structured analysis.
3. Key SQL Analysis
•	Revenue by Gender: Identified that Male customers contribute higher total revenue ($157,890) compared to Female customers ($75,191).
•	High-Value Discount Users: Identified top 20 customers who use discounts but still spend above the average purchase amount.
•	Product Performance: Determined that Gloves (3.86) and Sandals (3.84) hold the highest average review ratings.
________________________________________
📊 Power BI Dashboard Highlights
The interactive dashboard provides a visual narrative of the business.
Business KPIs
•	Total Customers: 3.9K.
•	Avg. Purchase Amount: $59.76.
•	Avg. Review Rating: 3.75/5.
Visual Insights
•	Category Dominance: Clothing is the primary revenue driver (~$100K+), while Outerwear is the lowest (~$15K+).
•	Subscription Gap: Only 27% of customers are currently subscribers, representing a significant growth opportunity.
•	Core Demographic: Young Adults are the most active buyers and contribute the highest revenue segment (~$60K+).
________________________________________
💡 Strategic Recommendations
1.	Subscription Growth: Promote loyalty programs to the 73% non-subscriber base to increase recurring revenue.
2.	Targeted Marketing: Focus campaigns on the Young Adult and Middle-Aged segments, as they show the highest engagement.
3.	Category Strategy: Implement promotional discounts for the Outerwear category to improve its market performance.
4.	Retention: Establish loyalty programs specifically targeting "Loyal" customers (those with >5 previous purchases).
________________________________________
🚀 Conclusion
This end-to-end project demonstrates how data cleaning and integrated analysis can identify high-value customer segments and product opportunities. By optimizing the subscription model and focusing on top-performing categories, the business can significantly enhance customer engagement and total revenue.
Created by: Nilesh Patil 

