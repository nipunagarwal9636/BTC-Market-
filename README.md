#  Bitcoin Market Sentiment & Trader Performance Analysis

## Project Overview
This project analyzes the relationship between **Bitcoin market sentiment** (Fear & Greed Index) and **trader performance** using historical trading data from Hyperliquid.  
The objective is to uncover behavioral patterns, quantify performance differences across sentiment regimes, and derive **actionable, sentiment-aware trading strategies**.

---

##  Objectives
- Analyze how trader profitability varies across sentiment regimes  
- Quantify the impact of sentiment on trading performance  
- Identify behavioral trader clusters  
- Translate insights into actionable trading and risk-management strategies  

---

##  Datasets

###  Bitcoin Market Sentiment Dataset
**File:** `fear_greed_index.csv`

| Column | Description |
|------|------------|
| Date | Calendar date |
| Classification | Sentiment category (Fear, Greed, etc.) |

Sentiment Encoding:
- Extreme Fear → 0  
- Fear → 25  
- Neutral → 50  
- Greed → 75  
- Extreme Greed → 100  

---

###  Historical Trader Data (Hyperliquid)
**File:** `historical_data.csv`

Key Columns:
- `account` – Trader identifier  
- `time` – Trade timestamp  
- `execution price` – Trade execution price  
- `size` – Trade size  
- `side` – Buy/Sell  
- `closedPnL` – Profit or loss per trade  
- `leverage` – Position leverage  

---

##  Methodology

###  Data Processing
- Timestamp normalization
- Daily aggregation (account-day level)
- Merge trader performance with daily market sentiment

###  Analytical Techniques
- Exploratory Data Analysis (EDA)
- **OLS Regression**
  - Target: Daily Gross PnL
  - Predictors: Sentiment, Trade Count
- **ANOVA**
  - Compare PnL across sentiment regimes
- **K-Means Clustering**
  - Group traders based on performance and activity patterns

---

##  Outputs

