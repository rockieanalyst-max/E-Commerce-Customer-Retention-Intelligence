# 📊 E-Commerce Customer Retention Intelligence (Power BI & RFM Analysis)

An end-to-end customer retention dashboard and RFM behavioral framework built in Power BI to optimize repeat purchasing, reduce churn risk, and deliver operational customer lists for targeted CRM campaigns.

---

## 🎯 Business Problem & Project Objective
Management lacked visibility into customer repeat-purchase behavior, cohort retention, and churn risk. Total sales metrics hid underlying customer drop-off.

**Key Objectives:**
- Isolate active registered customer behavior by filtering out guest transactions ($101.14K net sales / 1,407 orders).
- Implement dynamic RFM (Recency, Frequency, Monetary) segmentation across 9,607 registered customers ($3.11M completed net sales).
- Quantify revenue at risk and deliver an interactive, 3-page reporting layer with operational drill-through capabilities.

---

## 📈 Key Business Insights & Financial Impact
- **Revenue at Risk:** Identified **$1.16M (37.4% of total revenue)** sitting in the **At-Risk segment** (3,593 customers with high historical value but 120+ days of inactivity).
- **Champion Concentration:** **520 Champions** account for **$396.35K in revenue** with an average spend of **$762.22** (2.35x higher than average users).
- **Onboarding Bottleneck:** Identified a critical second-purchase drop-off, with **Potential Loyalists** representing less than 1% of total sales volume.

---

## 💻 Interactive Dashboard Architecture

### Page 1: Retention Executive Overview
Provides leadership with high-level KPI benchmarks, monthly sales trends, segment distribution, payment method breakdowns, geographic hubs, and cohort performance.

### Page 2: RFM Behavioral Matrix & Deep-Dive
Spatial scatter plot mapping Recency vs. Net Sales, benchmark matrix, age profile distribution, and a 5x5 RFM score heatmap grid.

### Page 3: Actionable Customer Directory & Drill-Through
Operational layer allowing CRM teams to right-click drill-through into any segment, view individual customer activity, and export clean lists for automated campaigns.

---

## 🛠️ Data Architecture & Tech Stack
- **Business Intelligence:** Power BI Desktop, DAX, Data Modeling (Star Schema), Power Query.
- **Segmentation Engine:** Dynamic DAX RFM Scoring (1–5 scale) mapped into 6 core segments.
- **Data Quality & Logic:**
  - `OrderStatus = "Completed"`
  - `CustomerID is not blank`
  - Order grain enforced via `DISTINCTCOUNT(fact_orders[OrderID])`.

---

## 📋 Strategic Marketing Playbook

| Customer Segment | Active Count | Net Revenue | Strategic Goal | Campaign Trigger & Action |
| :--- | :---: | :---: | :--- | :--- |
| **At Risk** | 3,593 | $1.16M | Urgent Win-Back | Automated 3-stage email/SMS sequence at 90, 120, and 150 days inactive. |
| **Loyal Customers** | 3,993 | $1.37M | Basket Expansion | Product bundling and threshold discounts ("Spend $100, Save $15"). |
| **Champions** | 520 | $396.35K | VIP Retention | Exclusive drops, early access, and dedicated support (no heavy discounting). |
| **Potential Loyalists** | 200 | $23.29K | 2nd-Purchase Conversion | Automated post-purchase onboarding with a 14-day bounce-back coupon. |

---

## 🚀 How to Explore
1. Clone this repository.
2. Open `powerbi/Customer_Retention_Dashboard.pbix` in Power BI Desktop.
3. Test right-click drill-through on Page 1 or 2 to inspect Page 3 directory filtering.
