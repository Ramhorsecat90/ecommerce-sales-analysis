# 🛒 E-Commerce Sales Analysis

## 📝 Overview
This project transforms raw user activity logs from an e-commerce site into meaningful business metrics to improve conversion and retention. Using advanced spreadsheet techniques and Tableau dashboards, the analysis identifies key bottlenecks in the purchase funnel and tracks customer behavior through cohort-based retention analysis.

## 🎯 Objectives
- Build a user conversion funnel to analyze how visitors move from product views to purchases.
- Prepare and transform raw event data into monthly acquisition cohorts.
- Calculate customer retention rates across a 4-month window post-acquisition.
- Deliver a professional-grade, executive-facing report and interactive Tableau dashboard.

## 📁 Dataset Description
- **Source**: Simulated user activity logs from an e-commerce website.
- **Sheet**: `raw_user_activity`
- **Columns**:
  - `user_id`: Unique customer identifier
  - `event_type`: Type of user interaction (view, cart, purchase)
  - `category_code`, `brand`, `price`, `event_date`

## 📊 Key Sheets and Analyses

### 🔻 Conversion Funnel (`conversion_funnel`)
- Built a 3-step funnel: product view → cart → purchase
- Used PivotTables to count **unique users** at each stage
- Calculated:
  - **Total conversion rate** from view to purchase
  - **Step-by-step conversion rates** (view → cart, cart → purchase)

### 🧮 Purchase Activity & Cohort Setup (`purchase_activity`)
- Filtered only **purchase events** from the raw data
- Created:
  - `first_purchase_date` using `VLOOKUP` from pivot in `first_purchase`
  - `event_month`, `first_purchase_month`, and `cohort_age` columns

### 👥 Cohort Analysis (`cohort_analysis`)
- Grouped users into **monthly cohorts** based on their first purchase
- Counted **unique returning users** across 0–4 months

### 📈 Retention Rates (`retention_rates`)
- Calculated retention for each cohort by dividing returning users by original cohort size
- Summarized 1–4 month retention rates for 6 acquisition cohorts

### 📉 Tableau Dashboard
Interactive Tableau dashboard created to visualize:
- 📊 Conversion Funnel: Step-by-step drop-offs in user journey
- 📈 Retention Analysis: Multi-line cohort chart showing user loyalty over time

> 🔗 [View Tableau Dashboard](https://public.tableau.com/app/profile/kenneth.weeks/viz/E-CommerceSalesAnalysisv2/Dashboard1)

## 🔍 Key Insights
- ~22% of users who added items to cart did not complete checkout
- Overall purchase conversion rate from product view was **10.34%**
- Users acquired in November–December cohorts showed stronger retention through Month 3
- Long-term retention across cohorts averaged **35–45%**

## 💡 Recommendations
- Reduce cart abandonment with reminder emails or UX improvements
- Enhance product pages to encourage initial engagement
- Target Q2 and Q3 cohorts with retention campaigns in Month 2

## 🛠️ Tools Used
- **Google Sheets / Excel**: Pivot Tables, VLOOKUP(), TEXT(), DATEDIF()
- **Tableau**: Conversion funnel, cohort retention visualization
- Spreadsheet design best practices (frozen headers, styling, sheet order)

## 🗂 Sheet Structure
| Sheet Name           | Description                                                  |
|----------------------|--------------------------------------------------------------|
| Table of Contents     | Quick navigation and layout summary                         |
| Executive Summary     | Key results and analysis explanations                       |
| conversion_funnel     | Conversion funnel pivot table and metrics                   |
| retention_rates       | Retention rate calculations by cohort and month             |
| purchase_activity     | Cleaned and prepared dataset for cohort analysis            |
| cohort_analysis       | Cohort user count pivot by age                              |
| first_purchase        | Pivot table of each user’s first purchase date              |
| raw_user_activity     | Original event log data (views, carts, purchases)           |

