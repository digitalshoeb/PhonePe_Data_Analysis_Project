# PhonePe_Data_Analysis_Project

Project Overview

This project involves a comprehensive end-to-end data analysis of PhonePe's transaction and user data using Power BI. By analyzing millions of UPI transactions—including recharges, bill payments, and money transfers—this project identifies key growth drivers, revenue trends, and user demographics
. The resulting interactive dashboard provides actionable insights into service promotion and regional performance for data-driven decision-making
.

Business Requirements
The objective was to track Key Performance Indicators (KPIs) and develop detailed visualizations to answer critical business questions:

- KPIs: Total Transaction Value, Total Number of Transactions, Transaction Success Rate (%), and Total Unique Users
.

- Performance Metrics: Month-over-Month (MoM) growth for both transaction volume and value to identify seasonal trends
.

- User Segmentation: Analysing activity by Age Segments (Gen Z, Millennials, Gen X, and Boomers) and transaction timing (Weekday vs. Weekend)
.

- Service Analysis: Identifying which services (e.g., Loans, Insurance, Money Transfer) generate the highest revenue
.

Technical Workflow

1. Data Cleaning & Transformation (Power Query)

- Data Ingestion: Processed a large-scale dataset of over 300,000 rows across two primary tables: All Users and All Transactions
.

- Profiling & Cleaning: Utilized Power Query Editor to check for empty values and ensure data quality
.

- Standardisation: Standardised labels by replacing underscores in service names (e.g., "Recharge_Bills" to "Recharge Bills") to ensure user-friendly visuals
.

- Error Handling: Handled inconsistent payment statuses by grouping "Wrong Pin," "Server Error," and "Insufficient Amount" into a single "Pending" category for clearer analysis
.

2. Data Modeling & DAX

- Schema Design: Established a One-to-Many relationship between the All Users and All Transactions tables using User ID
.

- Custom Date Table: Engineered a robust Date_Table using DAX (ADDCOLUMNS, CALENDAR) to facilitate time-intelligence functions like MoM growth
.

- Measure Creation: Developed a dedicated Measures Table containing over 50+ DAX calculations for metrics such as successful transaction rates and distinct user counts
.

- Feature Engineering: Created a Calculated Column for Age Segment to classify users into distinct demographic groups (e.g., Gen Z for those ≤ 26)
.

3. Dashboard Features & Interactivity

- Advanced Tooltips: Implemented hover-activated tooltips that provide granular insights without cluttering the main dashboard, such as specific loan types (Bike, Home, Car) within the broader "Loan" category
.

- Trend Visualisation: Created line charts to track seasonality and growth patterns in transaction values across the quarters of 2024
.

- Top Performance Tracking: Built a ranking system to identify the Top 5 Users by transaction value for potential loyalty rewards
.

Key Insights

- High-Value Services: Loans and Insurance emerged as the top contributors to total transaction value, suggesting PhonePe should prioritise these services for promotion
.

- Dominant Demographics: The Gen X and Millennial generations are the most active user groups, representing the largest share of the application's user base
.

- Transaction Timing: Approximately 72% of transactions occur during the weekdays, compared to 28% on weekends
.

- Operational Health: The platform maintains a high 96% success rate, with remaining failed or pending transactions often tied to server issues or insufficient funds
.

Tools Used
- Power BI Desktop: For data visualisation and report authoring.
- Power Query (M): For ETL processes and data cleaning.
- DAX (Data Analysis Expressions): For advanced business logic and KPI modeling.
- Excel: As the underlying data source for users and transactions.
