# Marketing Analytics with Python
An end-to-end marketing analytics project analysing Meta Ads 
campaign performance and customer behaviour using Python.


---

## Project Overview
This project takes raw Meta Ads data and CRM customer data 
through a complete analytics pipeline — from messy raw exports 
to clean, actionable business insights with professional visualisations.

---

## Datasets
- **Meta Ads data** — 16 rows, 4 campaigns, 4 weeks of January 2024
- **CRM Customer data** — 15 customers across 4 Kenyan cities

---

## Module 1 — Pandas for Campaign Data

### What Was Done
- Loaded raw Meta Ads export from Excel into Python
- Identified and fixed 3 data quality issues:
  - Missing impression values
  - Invalid text (UNKNOWN) in conversions column
  - Wrong data types — dates as text, numbers as objects
- Calculated key marketing metrics from scratch:
  - CTR — Click Through Rate
  - CPC — Cost Per Click
  - ROAS — Return on Ad Spend
  - Conversion Rate
- Exported clean stakeholder report to Excel

### Campaign Performance Results
| Campaign | Spend | Revenue | ROAS | Avg CTR | Avg CPC |
|---|---|---|---|---|---|
| Retargeting - Dynamic | $2,325 | $37,110 | 15.96x | 6.66% | $0.18 |
| Summer Sale - Video | $4,935 | $18,750 | 3.80x | 2.21% | $0.37 |
| Summer Sale - Carousel | $3,600 | $9,950 | 2.76x | 1.88% | $0.47 |
| Brand Awareness - Video | $2,645 | $1,520 | 0.57x | 0.50% | $0.63 |

### Module 1 Recommendations
1. **Increase budget for Retargeting - Dynamic** — ROAS of 15.96x,
   cheapest clicks at $0.18
2. **Maintain Summer Sale - Video** — solid 3.80x ROAS, good conversions
3. **Review Summer Sale - Carousel** — weaker than Video on every metric
4. **Reframe Brand Awareness measurement** — low ROAS but builds 
   the audience Retargeting later converts

---

## Module 2 — Data Wrangling & CRM Merge

### What Was Done
- Merged Meta Ads performance data with CRM customer data on campaign name
- Resolved duplicate channel column issue after merge
- Analysed purchase value by campaign, customer type and location

### Customer Analysis Results
| Campaign | Avg Purchase Value | Total Purchase | Customers | Type |
|---|---|---|---|---|
| Retargeting - Dynamic | $9,300 | $186,000 | 20 | Returning |
| Summer Sale - Video | $4,600 | $73,600 | 16 | New |
| Summer Sale - Carousel | $2,567 | $30,800 | 12 | New & Returning |
| Brand Awareness - Video | $350 | $4,200 | 12 | New |

### Location Analysis Results
| City | Total Purchase | Avg Purchase | Customers |
|---|---|---|---|
| Nairobi | $129,800 | $5,408 | 24 |
| Mombasa | $66,000 | $5,500 | 12 |
| Kisumu | $59,200 | $4,933 | 12 |
| Nakuru | $39,600 | $3,300 | 12 |

### Module 2 Recommendations
1. **Returning customers spend 2x more than new customers** —
   invest in retention and loyalty programmes
2. **Target Mombasa more aggressively** — highest average
   purchase value per customer at $5,500
3. **Retargeting attracts the highest value customers** —
   $9,300 average purchase vs $350 for Brand Awareness

---

## Module 3 — Exploratory Data Analysis & Visualisation

### What Was Done
- Built 5 professional visualisations using Matplotlib and Seaborn
- Analysed ROAS, spend vs revenue, weekly trends,
  city purchase value and metric correlations

### Chart Findings

**Chart 1 — ROAS by Campaign**
Retargeting - Dynamic at 15.96x towers over all other campaigns.
Visually confirms where budget should go immediately.

**Chart 2 — Spend vs Revenue**
Retargeting spent the least but generated the highest revenue.


**Chart 3 — Weekly ROAS Trend**
Retargeting stays consistently flat at 15-16x across all 4 weeks —
stable and reliable. All other campaigns show minor fluctuations
but no dramatic changes — performance is predictable.

**Chart 4 — Purchase Value by City**
Mombasa leads on average purchase value at $5,500 per customer.
Nakuru is the weakest market at $3,300 average.

**Chart 5 — Correlation Heatmap**
| Metric Pair | Correlation | Insight |
|---|---|---|
| Conversions vs Revenue | 0.99 | Almost perfect — conversions drive revenue |
| Revenue vs Purchase Value | 0.99 | High value customers = high revenue |
| Clicks vs Revenue | 0.84 | Quality clicks drive revenue |
| Spend vs Revenue | -0.28 | Spending more does NOT mean earning more |
| Impressions vs Revenue | -0.89 | High impressions = lower revenue |

### Module 3 Recommendations
1. **Focus on conversions not impressions** — 0.99 correlation with
   revenue vs -0.89 for impressions
2. **Retargeting is efficient AND consistent** — 15-16x ROAS
   every single week with no drop off
3. **Increase Mombasa targeting** — highest purchase value city
   with room to grow customer count

---

## Overall Analyst Recommendations

| Priority | Action | Reason |
|---|---|---|
| 1 | Increase Retargeting budget | 15.96x ROAS, $9,300 avg customer value |
| 2 | Invest in customer retention | Returning customers spend 2x more |
| 3 | Target Mombasa aggressively | Highest avg purchase value at $5,500 |
| 4 | Cut Summer Sale Carousel budget | Weakest performer vs Video |
| 5 | Reframe Brand Awareness KPIs | Measure reach not ROAS |
| 6 | Focus on conversion rate | 0.99 correlation with revenue |

---

## Modules Completed
- [x] Module 1 — Pandas for campaign data
- [x] Module 2 — Data wrangling & CRM merge
- [x] Module 3 — Exploratory data analysis & visualisation
- [ ] Module 4 — Customer segmentation
- [ ] Module 5 — Attribution & funnel analysis
- [ ] Module 6 — A/B testing
- [ ] Module 7 — Automated reporting
- [ ] Module 8 — Capstone project

---

## Tools Used
Python · Pandas · NumPy · Matplotlib · Seaborn · Jupyter Notebook · Excel

---

## Author
Joseph Mutua 
