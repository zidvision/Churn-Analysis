# Customer Churn Analysis for Online Retail

## Project Objective
To identify customers who have churned or are at risk of churning based on their purchasing behavior.  
This enables the business to take proactive actions such as re-engagement campaigns or loyalty incentives to reduce revenue loss and increase retention.

---

## Dataset Used
- `Online Retail`  
By: [Chen, D. (2015). Online Retail [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5BW33.](https://archive.ics.uci.edu/dataset/352/online+retail)

---

## Business Questions Answered
- How many customers have churned in the last period?
- Who are our active, at-risk, and lost customers?
- What strategies can we apply to re-engage lost or passive customers?
- How is churn distributed across customer segments?

---

## Process

### 1. Data Cleaning and Transformation
- Removed nulls, duplicates, and canceled transactions
- Converted data types (especially date columns) for consistent time-based analysis
- Created a `TotalPrice` column (`Quantity * UnitPrice`) for calculating spending

*[View cleaned dataset](https://github.com/zidvision/Churn-Analysis/blob/main/Data/Online_Retail_Cleaned.csv)*

---

### 2. Customer Monthly Activity Summary
Aggregated by `CustomerID` and `Year-Month` to calculate:
- Transaction Count
- Total Spend

---

### 3. Churn Status Classification
Defined churn based on `last active month`:
- **Active**: Last purchase within the last 30 days
- **At Risk**: Last purchase between 31–60 days ago
- **Churned (Lost)**: No purchases in over 90 days

*[View Customer Segmentation](https://github.com/zidvision/Churn-Analysis/blob/main/Data/Customer_Segmentation.csv)*

---

### 4. Visualization Creation
The visualization was created using Matplotlib library to visualize:
- Churn status distribution (Active, At Risk, Lost)

*[View Visualization](https://github.com/zidvision/Churn-Analysis/blob/main/Visualization/Customer%20Segmentation%20Distribution.png)*

---

## Key Insights
- Majority of customers are still active (44%). Nearly half of the total customer base is classified as active, indicating a healthy level of engagement. This presents a strong foundation for retention, upselling, and loyalty-building efforts.
- Churn rate is significantly high (40.9%). More than 2 out of 5 customers have churned. This highlights a potential revenue loss if no reactivation or win-back strategy is implemented.
- Relatively small portion of customers are “At Risk” (15.1%). Only a minority of customers are in the at-risk category. This offers a clear opportunity to intervene before they churn, through targeted campaigns such as limited-time offers, re-engagement emails, or personalized incentives.
- Churn and Active segments are nearly balanced (44% vs. 40.9%). This is a red flag: without a solid customer retention plan, active users may continue shifting into the churn category in the coming months.

---

## Conclusion
Understanding churn patterns enables the development of targeted retention strategies:
- Maintain Active customers with loyalty programs
- Re-engage At Risk customers before they churn
- Investigate churn reasons among Lost customers to improve future retention

---

## Tools and Libraries Used
- Python
- Pandas
- Matplotlib
- Jupyter Notebook
- Microsoft Excel
