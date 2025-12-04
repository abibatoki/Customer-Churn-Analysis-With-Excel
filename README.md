# 📉 Customer Churn Analysis with Excel

**🔍 Overall Churn Rate:** 27%  
**📊 Tools Used:** Excel PivotTables, Calculated Columns, Interactive Dashboard  

---

## 📘 Project Overview

This project analyzes customer churn for **Databel**, a fictional telecom company. The goal is to identify **who is churning**, **why they churn**, and **which segments require targeted retention strategies**.

### Workflow Includes:
- Data cleaning & transformation  
- New calculated fields for churn measurement  
- Demographic segmentation  
- Pivot-table exploration  
- Insight-driven visualization  
- Final interactive dashboard  

---

## 🛠 Tools & Techniques
- Microsoft Excel
- Pivot Tables and Pivot Charts
- Age grouping & segmentation
- Calculated fields
- Combo charts, donut charts, heat maps
- Dashboard design best practices

---

## 🧹 Data Preparation

Four key transformations were performed to prepare the dataset for analysis. These steps occur in the **Churn Analysis workbook** and serve as the foundation for all dashboard metrics.

### 1. Created a Binary Churn Indicator (Churned)
The original *Churn Label* field contained “Yes”/“No.”  
To enable numerical aggregation, a new column **Churned** was created using:

```excel
=IF([@Churn_Label]="Yes",1,0)
```

This allowed Excel to calculate churn totals, rates, and segment-based comparisons.

---

## 2. Calculated Customer-Level Churn Rate
A new **Churn Rate** column was added by dividing churned customers by total customers.  
Formatted to **percentage (two decimal places)** to support trend analysis and dashboard KPIs.

---

## 3. Created a Demographics Classification Column
A new **Demographics** field was derived using nested IF logic that categorizes customers into:

- Under 30  
- Senior (≥ 60)  
- Other  

**Example logic:**
```excel
=IF(Age<30,"Under 30",IF(Age>=60,"Senior","Other"))
```
This segmentation was later used to build pie charts and analyze churn patterns across age-related groups.

---

## 4. Grouped Age into 10-Year Bins

Within the pivot tables (**Customer Pivots workbook**), age was grouped using Excel’s **Group → By 10** function, producing:
```
19–28, 29–38, 39–48, 49–58, 59–68, 69–78, 79–88
```
These groups were essential for the **Churn by Age Group** chart.

---

# 📈 Exploratory Analysis

After preparing the data, several pivot-table–driven analyses were conducted across behavioral, demographic, and competitor-related metrics.

---

## 1. Churn by Age Group

A combination column–line chart visualized:

- Total customers per age range  
- Number of churned customers  
- Churn rate (%)  

💡 **Insight:** Younger (<30) and senior (>60) groups showed higher churn, highlighting the need for **age-specific experience strategies**.

---

## 2. Churn by Data Usage

Data usage was segmented into:

- < 5GB  
- 5–10GB  
- > 10GB  

Higher data users churn less, implying **greater value perception**.

---

## 3. Reasons for Churn

A horizontal bar chart revealed key causes:

- Competitor offering better devices  
- Competitor offering better deals  
- Higher competitor download speeds  
- Customer service dissatisfaction  

**Competitor-related reasons dominated** the churn causes.

---

## 4. Competitor Influence

A donut chart summarized churn driven by competitor factors, emphasizing the need for:

- Better retention offers  
- Device upgrade programs  

---

## 5. Churn Rate by State

Conditional formatting produced a **geographic heatmap**.  
States like **California** and **Indiana** showed the highest churn, guiding regional retention strategies.

---

## 6. Churn by Demographics

A pie chart compared churn across:

- Under 30  
- Senior  
- Other  

**Seniors had the highest churn**, while **Other** showed the lowest.

---
# 📊 Final Excel Dashboard
The final dashboard integrates all KPIs and visualizations:
- Total Customers
- Churned Customers
- Overall Churn Rate
- Top churn reasons
- Churn by contract type
- Churn by age group
- Churn by demographics
- Competitor analysis
- State churn heatmap

These visual insights allow stakeholders to identify trends quickly and inform data-driven retention strategies.

# 🔑 Key Insights
📌 1. Churn Decreases the Longer a Customer Stays

From the tenure analysis, churn follows a strong downward trend:

| Tenure Range (Months) | Churn Rate |
| --------------------- | ---------- |
| **1–12**              | 47.69%     |
| **13–24**             | 29.48%     |
| **25–36**             | 22.10%     |
| **73–84**             | 3.68%      |

This indicates that improving early-life customer experience is critical for long-term retention.

---

📌 2. Contract Type Has a Major Impact on Churn

Month-to-month contracts unsurprisingly show the highest churn, confirming the need for stronger value propositions for flexible-plan customers.

Customers in the **37–48 month** tenure range show the largest churn gap between One-Year and Two-Year contracts. This means customers around the **3–4 year** mark are far more likely to leave when on a short-term contract compared to a two-year plan.

**Sales** and **Marketing** can use this insight to roll out targeted multi-year contract incentives, especially for maturing accounts crossing the 3-year threshold.

---

📌 3. Competitor Pressure Is the Top Churn Driver

Customers reported leaving mainly because competitors offer:

- Better devices
- Better deals
- Higher download speeds
  
These findings strongly support competitive benchmarking and product strategy repositioning.

---
📌 4. High-Engagement Customers Are More Loyal

Heavy data users have significantly lower churn rates, suggesting they derive higher perceived value.

**Opportunity:** Promote usage-based bundles and personalized add-ons to increase engagement.

---
📌 5. Senior Customers Are the Most Likely to Churn

Churn peaks at almost 40% among seniors, which signals:

- A need for more intuitive support
- Simplified plans
- Better onboarding for older users

---

# 🎯 Business Impact & Strategic Value

These insights directly support:

- Targeted retention campaigns (tenure-based, demographic-based, contract-type-based)
- Customer lifecycle management enhancements
- Pricing & contract optimization
- Product and service experience improvements
- Competitive strategy alignment
  
This analysis demonstrates how data-driven decision-making, paired with strong business analytics, can transform customer retention strategies and unlock long-term value.

---

# 🧠 What I Learned

- Building a clean ETL workflow in Excel
- Transforming raw telecom data into insights
- Designing professional dashboards
- Understanding how segmentation impacts churn

---





