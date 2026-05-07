# Marketing Analytics with Python

An end-to-end marketing analytics project analysing Meta Ads 
campaign performance and customer behaviour using Python.

---

## Project Overview

This project takes raw Meta Ads data and CRM customer data 
through a complete analytics pipeline — from messy raw exports 
to clean, actionable business insights.

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
- Calculated key marketing metrics:
  - CTR — Click Through Rate
  - CPC — Cost Per Click
  - ROAS — Return on Ad Spend
  - Conversion Rate

### Campaign Performance Results
| Campaign | Spend | Revenue | ROAS | Avg CTR | Avg CPC |
|---|---|---|---|---|---|
| Retargeting - Dynamic | $2,325 | $37,110 | 15.96x | 6.66% | $0.18 |
| Summer Sale - Video | $4,935 | $18,750 | 3.80x | 2.21% | $0.37 |
| Summer Sale - Carousel | $3,600 | $9,950 | 2.76x | 1.88% | $0.47 |
| Brand Awareness - Video | $2,645 | $1,520 | 0.57x | 0.50% | $0.63 |

---

## Module 2 — Data Wrangling & CRM Merge

### What Was Done
- Merged ad performance data with CRM customer data on campaign name
- Resolved duplicate channel column issue after merge
- Analysed purchase value by campaign, customer type and location

### Customer Analysis Results
| Campaign | Avg Purchase Value | Customer Type |
|---|---|---|
| Retargeting - Dynamic | $9,300 | Returning |
| Summer Sale - Video | $4,600 | New |
| Summer Sale - Carousel | $2,567 | New & Returning |
| Brand Awareness - Video | $350 | New |

### Location Analysis Results
| City | Total Purchase | Avg Purchase | Customers |
|---|---|---|---|
| Nairobi | $129,800 | $5,408 | 24 |
| Mombasa | $66,000 | $5,500 | 12 |
| Kisumu | $59,200 | $4,933 | 12 |
| Nakuru | $39,600 | $3,300 | 12 |

---

## Analyst Recommendations

1. **Increase budget for Retargeting - Dynamic** — ROAS of 15.96x
   and highest customer purchase value at $9,300 average
2. **Returning customers spend 2x more than new customers** —
   invest in retention and loyalty programmes
3. **Target Mombasa more aggressively** — highest average
   purchase value per customer at $5,500
4. **Reframe Brand Awareness measurement** — low ROAS but
   builds the audience that Retargeting later converts

---

## Modules Completed
- [x] Module 1 — Pandas for campaign data
- [x] Module 2 — Data wrangling & CRM merge
- [ ] Module 3 — Exploratory data analysis
- [ ] Module 4 — Customer segmentation
- [ ] Module 5 — Attribution & funnel analysis
- [ ] Module 6 — A/B testing
- [ ] Module 7 — Automated reporting
- [ ] Module 8 — Capstone project

---

## Tools Used
Python · Pandas · NumPy · Jupyter Notebook · Microsoft Excel

---

## Author
Joseph Mutua | github.com/mutua6
