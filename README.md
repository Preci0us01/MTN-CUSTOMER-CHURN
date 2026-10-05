# 📊 MTN CUSTOMER CHURN ANALYSIS(Q1 2026)

## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning/Preparation](#data-cleaningpreparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results/Findings](#resultsfindings)
- [Recommendations](#recommendation)
- [Limitations](#limitations)
- [References](#references)
  

### Project Overview

This project presents an interactive **Power Bi Dashboard** built to analyse customer churn, revenue distribution,
subscriber demographics and service performance for MTN during the first quarter of 2026. The goal is to uncover behaviourial patterns among subscribers, identify high-value customer segments, and highlight primary drivers of churn to help guide guide retention strategies.

### Data Sources

The primary dataset used for this analysis is the "mtn_customer_churn.csv" file, containing detailed information is obtained from a structured telecommunication dataset


### Tools

- Excel - Data cleaning [Download here](https://microsoft.com)
- SQL Server - Data Analysis [Download here](https://mysqlserver.com)
- PowerBI - Writing DAX & Data Visualisation


### Data Cleaning/Preparation

In the initial data preparation phase, we performed the following tasks:
1. Data loading and Inspection
2. Handling missing values
3. Data Cleaning and formatting


### Exploratory Data Analysis

EDA  involved exploring the mtn customer churn data to answer key questions, such as:

- Total revenue generated across different parameter
- Customer Churn Distribution
- Best Subscriber And Best State
- Customer Satisfaction rating 

### Data Analysis

Include some interesting code/feature worked with

```sql
CREATE VIEW MTN AS
SELECT *,
ROW_NUMBER () OVER(
PARTITION BY customer_id,mtn_device,subscription_plan)AS duplicate
FROM mtn_customer_churn ;
```

### Results/Findings

The analysis results are summarised as follow;
1. The active subscriber base leans towards a mature demographic, with an average age of **48 years**.
2. High call tariffs (160 users) and costly data plans(132 users) acts as major financial frictions.
3. Infrastructure constraints such as **Poor network coverage (147 users)**, **Slow data consumption speeds(126 users)**, and **Poor customer services (116 users)** heavily speed up customer drop-off.
4. Customer experience reviews heavily cluster around **Good(212 users)** and **Fair(199 users),** translating to an average rating score of 3 out of 5 stars.
5. **MTN** generated **₦199.35** in total revenue, tracking against broader quaterly objectives.
6. State analysis indicates widespread national reach, with **Plateau State** emerging as the best performing state for revenue generation.
7. Out of 974 total subscribers analyzed, **284 customers(approx. 29%)** have churned,leaving an active subscriber base of 690 users.


### Recommendation

Based on the analysis, I recommend the following actions;


1. Address the 29% churn rate by introducing loyalty discounts or bundled bonuses to counter competitive pricing ("Better Offers").
2. Prioritise infrastructure upgrades in region experiencing high churn due to "Poor Network Coverage and "Slow data speeds".
3. With poor customer service driving 116 churned users, implement faster ticketing workflows, proactive issue resolution, and follow up check-ins for users reporting "fair" or "poor" satisfaction rate.
4. Leverage the high revenue yield seen in 5G routers (100.82M) by running upgrade campaigns that offer affordable instalment plan or trade-in incentives for users on standard SIM or basic MiFi devices. 

### Limitations

1. They were some missing data.



 ### References

1. **Microsoft PowerBi documentation** - Guidelines for DAX Measures and data Modelling
2. **Kaggle dataset** - *MTN Customer Churn(Q1 2026)*



