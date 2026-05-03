# Marketing Analytics with Python 

### Dataset
A Meta Ads export covering 4 campaigns across January 2024.
16 rows of weekly performance data across 8 columns:
campaign_name, channel, impressions, clicks, spend, conversions, revenue, date.

### Data Quality Issues Found
| Issue | Column | Details |
|---|---|---|
| Missing value | impressions | Summer Sale Carousel — 21 Jan had no impression data |
| Invalid text | conversions | Retargeting Dynamic — 28 Jan had "UNKNOWN" instead of a number |
| Missing value | conversions | Brand Awareness Video — 14 Jan was blank |
| Wrong data type | date | Loaded as object (text) instead of datetime |
| Wrong data type | conversions | Loaded as object due to UNKNOWN value |
| Wrong data type | impressions | Loaded as float64 instead of int due to null |

### How I Fixed Them
- Converted date column to datetime using pd.to_datetime()
- Replaced UNKNOWN with NaN then converted conversions to numeric
- Filled missing impressions using the median of that campaign using groupby + transform
- Converted impressions to int64 after nulls were resolved

### Marketing Metrics Calculated
- **CTR** — Click Through Rate = clicks / impressions × 100
- **CPC** — Cost Per Click = spend / clicks
- **ROAS** — Return on Ad Spend = revenue / spend
- **Conversion Rate** = conversions / clicks × 100

### Key Findings

| Campaign | Total Spend | Total Revenue | ROAS | Avg CTR | Avg CPC |
|---|---|---|---|---|---|
| Retargeting - Dynamic | $2,325 | $37,110 | 15.96x | 6.66% | $0.18 |
| Summer Sale - Video | $4,935 | $18,750 | 3.80x | 2.21% | $0.37 |
| Summer Sale - Carousel | $3,600 | $9,950 | 2.76x | 1.88% | $0.47 |
| Brand Awareness - Video | $2,645 | $1,520 | 0.57x | 0.50% | $0.63 |

### Analyst Recommendations
1. **Increase budget for Retargeting - Dynamic** — highest ROAS at 15.96x, 
   cheapest clicks at $0.18. Every $1 spent returns $15.96 in revenue.
2. **Maintain Summer Sale - Video** — solid 3.80x ROAS, good volume of conversions.
3. **Review Summer Sale - Carousel** — similar spend to Video but weaker on every metric.
   Consider reallocating its budget to Retargeting.
4. **Reframe Brand Awareness measurement** — 0.57x ROAS looks poor but this campaign 
   builds the audience that Retargeting later converts. 
   Measure by reach and frequency, not direct revenue.

### Files
- `data/meta_ads_raw.csv` — original raw dataset
- `notebooks/module1_pandas_campaign_data` — full analysis notebook
- `outputs/meta_ads_report.xlsx` — cleaned data and summary exported to Excel



## Author
mutua6 | Marketing Analytics Training Portfolio
