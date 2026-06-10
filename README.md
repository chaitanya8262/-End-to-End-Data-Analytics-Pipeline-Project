🏦 Banking Dashboard
A end-to-end data analytics project that transforms raw banking data into an interactive Power BI dashboard — covering client loans, deposits, fees, and engagement metrics.

📌 Project Overview
This project analyzes banking client data to uncover insights across loan portfolios, deposit accounts, and client engagement. The final output is a multi-page Power BI dashboard with drill-through capability, enabling stakeholders to filter and explore data by gender, period, banking relationship, and investment advisor.

🛠️ Tech Stack
LayerToolRaw DataCSV / Excel FilesData Cleaning & TransformationPython (Jupyter Notebook)Data Querying & AggregationSQLVisualizationPower BI (.pbix)

🔄 Pipeline Steps
1. Raw Data (CSV/Excel)

Source files containing client-level banking data
Fields include client demographics, account types, loan amounts, deposit balances, fees, and engagement history

2. Data Cleaning — Jupyter Notebook

Loaded raw CSV/Excel files using pandas
Handled missing values, duplicates, and data type conversions
Engineered features such as engagement timeframe, income band classification, and loyalty classification
Exported cleaned data for SQL ingestion

3. SQL Aggregations

Wrote queries to aggregate metrics by nationality, income band, banking relationship, and period
Computed key measures: total loans, deposits, fees, credit card amounts, and savings balances
Final output tables loaded into Power BI data model

4. Power BI Dashboard

Built DAX measures for all KPIs
Designed 5 report pages with slicers, cards, and charts
Enabled drill-through for client-level analysis


📊 Dashboard Pages
🏠 Home
Overview page with top-level KPI cards and navigation buttons to other report pages.
Metrics: Total Clients, Total Loan, Total Deposit, Total CC Amount, Total Fees, Savings Account
Filters: Gender, Period

💳 Loan Analysis
Deep dive into the bank's loan portfolio across client segments.
Metrics: Total Loan, Bank Loan, Credit Cards, Business Lending
Visuals:

Donut Chart — Bank Loan by Income Band
Clustered Bar Chart — Total/Bank/Business Lending by Engagement Timeframe
Treemap — Bank Loan by Nationality
Line + Column Combo Chart — Bank Loan by Banking Relationship

Filters: Banking Relationship, Gender, Investment Advisor, Period

🏦 Deposit Analysis
Analysis of client deposit behavior across account types and segments.
Metrics: Total Deposit, Bank Deposit, Savings Account, Checking Accounts, Foreign Currency Account
Visuals:

Treemap — Bank Deposit by Income Band
Column Chart — Total/Bank Deposit & Savings by Nationality
Clustered Bar Chart — Total Deposit by Engagement Timeframe

Filters: Banking Relationship, Gender, Investment Advisor, Period

📋 Summary
Consolidated view of all KPIs in one place for quick stakeholder reporting.
Metrics: Engagement Length, Foreign Currency Account, Bank Deposit, Checking Accounts, Bank Loan, Business Lending, Savings Account, Total CC Amount, Total Deposit, Total Fees, Total Clients, Total Loan
Filters: Banking Relationship, Gender, Investment Advisor, Period

🔍 Drill Through
Client-level detail page accessible via drill-through from other report pages.
Visuals:

Table — Client Name, Investment Advisor, Engagement Length, Total Fees
Column Chart — Total Fees by Loyalty Classification
Column Chart — Total Fees & Engagement Length by Nationality

Filters: Banking Relationship, Gender, Investment Advisor, Period

📐 Data Model
Fact Table: Clients - Banking
Dimension Tables:
TableKey FieldBanking RelationshipBanking RelationshipGenderGenderInvestment AdvisorInvestment AdvisorPeriodName
Key Dimensions: Nationality, Income Band, Loyalty Classification, Engagement Timeframe

📏 DAX Measures
MeasureDescriptionTotal ClientsCount of all banking clientsTotal LoanSum of all loan amountsTotal DepositSum of all deposit balancesBank LoanBank-issued loan totalBank DepositBank deposit totalBusiness LendingBusiness loan totalCredit CardsCredit card balance totalSavings AccountSavings account balance totalChecking AccountsChecking account balance totalForeign Currency AccountForeign currency account totalTotal FeesTotal fees collectedTotal CC AmountTotal credit card amountEngagement LengthAverage client engagement duration
