# 🚀 Customer Onboarding Process Optimization & Revenue Forecasting


**Project Type:** Business Operations Senior Analyst Portfolio Project  
**Tools:** Power BI, Excel, Python, DAX

---

## 📌 Project Overview

This project simulates a real-world Business Operations Senior Analyst case study for a SaaS company, analyzing customer onboarding delays, identifying root causes, and forecasting revenue impact. 

It demonstrates hands-on data analytics, business storytelling, and financial modeling skills required for Senior Analyst and Business Operations roles.

---

## 🎯 Business Problem

The company is facing:

- Increasing onboarding delays
- Delayed revenue recognition
- Higher churn risk
- Loss of operational efficiency

The objective was to:

- Analyze onboarding process by team, segment, and delay group
- Correlate onboarding delays with churn behavior
- Quantify revenue delay and lost opportunities
- Build actionable recommendations for leadership

---

## 🔧 Data Description

Synthetic dataset generated with 200 simulated SaaS customer records.

| Column | Description |
|--------|-------------|
| Customer_ID | Unique identifier |
| Onboarding_Start_Date | Start date of onboarding |
| Onboarding_End_Date | End date of onboarding |
| Onboarding_Duration_Days | Days taken for onboarding |
| Assigned_Onboarding_Team | Assigned team (A, B, C) |
| Industry_Segment | Enterprise, SMB, Startup |
| Contract_Value | Customer contract value |
| Revenue_Recognition_Date | Revenue start date |
| Churn_Flag | Customer churn status (Yes/No) |
| Delay_Flag | High Delay (>15 days), Low Delay (<=15 days) |

---

## 📊 Analysis & Modeling Steps

1️⃣ **KPI Calculation**
- Avg onboarding duration
- Avg contract value
- Total revenue at risk
- Churn % by delay group

2️⃣ **Root Cause Analysis**
- Bottlenecks by team
- Segment-wise performance
- Churn correlation with delays

3️⃣ **Revenue Forecast Model**
- Modeled financial impact of reducing onboarding time
- Forecasted revenue acceleration potential

4️⃣ **Power BI Executive Dashboard**
- KPI summary cards
- Duration analysis by team & segment
- Churn % analysis by delay flag
- Revenue forecast table

---

## 🧮 Key Formula (DAX)

**Churn % Measure (Power BI):**

```DAX
Churn = 
DIVIDE(
    CALCULATE(
        COUNTROWS('BizOps_Onboarding_PowerBI_Template'),
        FILTER(
            'BizOps_Onboarding_PowerBI_Template',
            'BizOps_Onboarding_PowerBI_Template'[Churn_Flag] = "Yes"
        )
    ),
    COUNTROWS('BizOps_Onboarding_PowerBI_Template')
)
