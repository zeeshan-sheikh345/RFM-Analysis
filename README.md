# **RFM Analysis**

---

### **What is RFM Analysis?**

RFM analysis is a **customer segmentation technique** used in marketing to identify and prioritize customers based on their purchasing behavior. It helps businesses:

- Target high-value customers for loyalty programs.
- Identify inactive customers for re-engagement campaigns.
- Optimize marketing spend by focusing on profitable segments.

RFM stands for:

- **Recency (R):** How recently a customer made a purchase.
- **Frequency (F):** How often a customer makes purchases.
- **Monetary (M):** How much money a customer spends.

---

### **Why RFM Analysis is Important**

- **Customer Lifetime Value (CLV):** RFM helps estimate CLV.
- **Personalized Marketing:** Enables tailored campaigns for different segments.
- **Retention Strategies:** Identifies churn risk early.

---

### **Steps in RFM Analysis**

1. **Collect Transaction Data:** Customer ID, purchase date, purchase amount.
2. **Calculate RFM Metrics:**
    - **Recency:** Days since last purchase.
    - **Frequency:** Number of purchases in a given period.
    - **Monetary:** Total spend in that period.
3. **Score Each Metric:**
    - Assign scores (e.g., 1–5) for R, F, and M based on quantiles.
4. **Combine Scores:**
    - Create an RFM score (e.g., `RFM = R + F + M` or as a tuple `(R,F,M)`).
5. **Segment Customers:**
    - High RFM score → VIP customers.
    - Low RFM score → At-risk customers.

---

### **Example with Demo Data**

### **Sample Transaction Data**

| CustomerID | LastPurchaseDate | TotalPurchases | TotalSpend |
| --- | --- | --- | --- |
| C001 | 2025-12-01 | 10 | $1,200 |
| C002 | 2025-11-15 | 5 | $500 |
| C003 | 2025-09-20 | 2 | $150 |
| C004 | 2025-12-08 | 15 | $2,000 |
| C005 | 2025-07-10 | 1 | $50 |

### **Step 1: Calculate Recency**

Assume today = 2025-12-10:

- C001: 9 days
- C002: 25 days
- C003: 81 days
- C004: 2 days
- C005: 153 days

### **Step 2: Assign Scores (1–5)**

- **Recency:** Lower days → higher score.
- **Frequency:** More purchases → higher score.
- **Monetary:** Higher spend → higher score.

| CustomerID | R | F | M | RFM Score | RFM score 2 |
| --- | --- | --- | --- | --- | --- |
| C004 | 5 | 5 | 5 | 15 | 555 |
| C001 | 4 | 4 | 4 | 12 | 444 |
| C002 | 3 | 3 | 3 | 9 | 333 |
| C003 | 2 | 2 | 2 | 6 | 226 |
| C005 | 1 | 1 | 1 | 3 | 111 |

### **Interpretation**

- **C004:** VIP customer (recent, frequent, high spender).
- **C005:** At-risk (old purchase, low frequency, low spend).

## Customer Segments

1. **Champions** (High R, F, M): Best customers who buy frequently and spend the most.
2. **Loyal Customers** (Moderate R, High F, M): Frequent buyers, but not recent.
3. **Potential Loyalists** (High R, Low-Mid F, M): Recently engaged but less frequent.
4. **At Risk** (Low R, Moderate F, M): Previously frequent buyers, recently inactive.
5. **Dormant** (Low R, F, M): Long-time inactive customers with low engagement.

## **Calculate RFM Scores**

For each customer, calculate a score (1-5) based on three factors:

- **Recency (R)**: How recently did they make a purchase?
- **Frequency (F)**: How often do they make purchases?
- **Monetary (M)**: How much money have they spent?

Higher scores (5) indicate recent, frequent, and high-spending customers. Use the combined RFM score (R+F+M) to segment customers into different groups.

### Customer RFM Score Table

| **Customer** | **Recency Score (R)** | **Frequency Score (F)** | **Monetary Score (M)** | **Total RFM Score** | **Segment** |
| --- | --- | --- | --- | --- | --- |
| Customer A | 5 | 5 | 5 | 15 | Champion |
| Customer B | 4 | 5 | 4 | 13 | Loyal |
| Customer C | 3 | 2 | 2 | 7 | At Risk |
| Customer D | 5 | 1 | 1 | 7 | New/Occasional |
| Customer E | 1 | 3 | 3 | 7 | Dormant |

### RFM Scoring Guide

**Scoring System for Recency, Frequency, and Monetary Values**

| Metric | Score 1 (Low) | Score 2 | Score 3 | Score 4 | Score 5 (High) |
| --- | --- | --- | --- | --- | --- |
| **Recency** | >6 months ago | 3-6 months ago | 1-3 months ago | 2 weeks - 1 month | Last week |
| **Frequency** | 1 purchase | 2-3 purchases | 4-5 purchases | 6-10 purchases | 11+ purchases |
| **Monetary** | <$50 | $50-$300 | $300-$1000 | $1000-$1500 | >$1500 |

### **How to Use RFM Segments**

- **VIP Customers:** Offer loyalty rewards.
- **Moderate Customers:** Upsell or cross-sell.
- **At-Risk Customers:** Send re-engagement campaigns.

---

✅ **Tip:** You can implement this in **Excel**, **SQL**, or **Python (Pandas)** for hands-on practice.

---
