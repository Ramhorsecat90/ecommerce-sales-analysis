# 🛒 E-Commerce Sales Analysis

## 📝 Overview
This project transforms raw user activity logs from an e-commerce site into meaningful business metrics to improve conversion and retention. Using advanced spreadsheet techniques, the analysis identifies key bottlenecks in the purchase funnel and tracks customer behavior through cohort-based retention analysis.

## 🎯 Objectives
- Build a user conversion funnel to analyze how visitors move from product views to purchases.
- Prepare and transform raw event data into monthly acquisition cohorts.
- Calculate customer retention rates across a 4-month window post-acquisition.
- Deliver a professional-grade, executive-facing report for strategic decision-making.

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

## 🔍 Key Insights
- ~22% of users who added items to cart did not complete checkout
- Overall purchase conversion rate from product view was **8.4%**
- Users acquired in Nov–Dec cohorts had stronger retention at months 2 and 3
- Long-term retention averaged **35–45%** over a 4-month period

## 💡 Recommendations
- Reduce drop-offs at the cart stage with targeted cart-abandonment campaigns
- Improve product page clarity and CTA strength to boost initial conversions
- Reinforce engagement with new customers during their second month

## 🛠️ Tools Used
- **Google Sheets / Excel**
  - Pivot Tables
  - VLOOKUP(), TEXT(), DATEDIF()
- Spreadsheet formatting best practices (frozen headers, borders, tab order)

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

## 🔄 Future Improvements
- Integrate marketing channel data to measure acquisition source impact
- Visualize funnel and retention metrics in Tableau or Power BI
- Build predictive churn models using Python or SQL for retention strategy

