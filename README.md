# RavenStack Customer Churn Analysis

> A complete end-to-end customer churn analysis for RavenStack — a fictional B2B SaaS platform — using real-world analytics techniques across five interconnected datasets.

---

## Project Overview

This project investigates why customers leave RavenStack's platform, which segments are most at risk, and what data-driven actions can improve retention. The analysis was built entirely from raw CSV data and visualized in **Power BI Desktop**.

**Key findings at a glance:**
- 📉 Overall churn rate: **22%** (110 of 500 customers)
- 💸 Estimated ARR at risk from churn: **$3.38 million**
- ⚠️ Highest-risk segment: **DevTools industry** (31% churn rate)
- 🌍 Highest-risk geography: **Germany** (32% churn rate)
- 🕐 Churn peaks after **12–18 months** on the platform
- 🔑 Top churn reasons: **Missing features**, **poor support experience**, and **budget constraints**

---

## Datasets

| File | Description | Rows |
|------|-------------|------|
| `ravenstack_accounts.csv` | Core account data — industry, country, plan, trial status, churn flag | 500 |
| `ravenstack_subscriptions.csv` | Subscription records with MRR, ARR, plan tier, upgrade/downgrade flags | 5,000 |
| `ravenstack_churn_events.csv` | Churn event log with reason codes, refund amounts, and feedback text | 600 |
| `ravenstack_support_tickets.csv` | Support ticket history with resolution times, priority, and satisfaction scores | 2,000 |
| `ravenstack_feature_usage.csv` | Feature-level usage logs with usage counts, duration, and error counts | 25,000 |

---

## Dashboard Pages

### Page 1 — Churn Overview
High-level KPIs and churn distribution across industries, plan tiers, countries, and trial status.

![Churn Overview Dashboard](./assets/dashboard_page1.png)

**Key visuals:**
- KPI cards: Active Customers, Churn Rate, Churned Customers, Retention Rate, Total Customers
- Bar chart: Churn rate by industry
- Pie chart: Churn rate by plan tier
- Pie chart: Churn rate by trial status (`is_trial`)
- Bar chart: Churn rate by country

### Page 2 — Customer Lifetime Analysis
How long customers stay active before churning, segmented by age band.

![Customer Lifetime Dashboard](./assets/dashboard_page2.png)

**Key visuals:**
- KPI cards: Median active age, median churned age, overall median and average tenure
- Horizontal bar chart: Churn rate by customer age band (0–3 months through 12–24 months)

---

## Key Insights

### 1. Who is churning?
- **DevTools** companies churn at nearly 31% — almost double the rate of Cybersecurity (16%)
- **Germany** leads geographically at 32%; **Australia** is the most loyal market at 12.5%
- **Trial users** churn at 25.8% vs. 21.1% for paid users — trial-to-paid conversion is a problem
- All three plan tiers (Basic, Pro, Enterprise) churn at nearly identical rates (~22%), suggesting plan pricing alone is not the driver

### 2. Why are they leaving?
Churn reasons are almost evenly distributed across five categories:

| Reason | Count | % of Churns |
|--------|-------|-------------|
| Missing Features | 114 | 19% |
| Poor Support | 104 | 17.3% |
| Budget Constraints | 104 | 17.3% |
| Unknown | 95 | 15.8% |
| Competitor Switch | 92 | 15.3% |
| Pricing Concerns | 91 | 15.2% |

### 3. When does churn happen?
- Active customers have a median tenure of **9.9 months**
- Churned customers had a median tenure of **12.5 months**
- Churn rate increases steadily from 0–3 months (~15%) to 12–24 months (~28%)
- This suggests a **12-month anniversary risk spike** — customers who didn't find enough value cancel around their first renewal

### 4. Revenue impact
- Total MRR at risk from churned customers: **$282,092**
- Annualised ARR impact: **$3,385,104**
- Churned accounts had slightly *higher* average MRR ($2,426) than active accounts ($2,251) — meaning higher-value customers are churning too

---

## Recommendations

1. **Feature roadmap alignment** — 19% of churns cite missing features. Run a feature gap survey with at-risk DevTools and FinTech accounts.
2. **Proactive 12-month check-ins** — Churn peaks at the 12–18 month mark. Schedule automated QBRs (Quarterly Business Reviews) before the first anniversary.
3. **Trial experience overhaul** — Trial users churn 4.7 points higher. Introduce guided onboarding, in-app checklists, and a human touchpoint at day 7.
4. **Germany market review** — At 32% churn, DE may have a product-market fit, pricing, or localization issue. Investigate with customer interviews.
5. **Support escalation reduction** — Churned accounts had a 5.6% escalation rate vs. 4.5% for active accounts. Faster first-response times could prevent escalations that lead to churn.

---

## Tools & Technologies

- **Power BI Desktop** — Data cleaning, Data Organizaton,Dashboard creation and visualization
- **CSV / Excel** — Raw data source format

---

## Folder Structure

```
ravenstack-churn-analysis/
│
├── data/
│   ├── ravenstack_accounts.csv
│   ├── ravenstack_churn_events.csv
│   ├── ravenstack_subscriptions.csv
│   ├── ravenstack_support_tickets.csv
│   └── ravenstack_feature_usage.csv
│
├── assets/
│   ├── dashboard_page1.png
│   └── dashboard_page2.png
│
├── RavenStack_Churn_Analysis.pbix
└── README.md
```

---

## Author

**[Mukhwana Sandra C]**    
[LinkedIn] www.linkedin.com/in/sandra-mukhwana-81b247116 · [Github] https://github.com/SandraCarol-droid

---

*This project uses a synthetic dataset created for portfolio and learning purposes. All company names and figures are fictional.*