# Hyperliquid Trader Performance vs. Market Sentiment Analysis

This repository contains a comprehensive data science assignment exploring the relationship between aggregate trader execution performance on Hyperliquid and daily Bitcoin Market Sentiment (Fear & Greed Index).

## 📊 Key Insights & Findings

| Market Sentiment | Total Trades | Win Rate (%) | Avg Position Size (USD) | Avg Closed PnL (USD) |
| :--- | :--- | :--- | :--- | :--- |
| **Extreme Fear** | 21,400 | 37.06% | $5,349.73 | $34.54 |
| **Fear** | 61,837 | 42.08% | $7,816.11 | $54.29 |
| **Neutral** | 37,686 | 39.70% | $4,782.73 | $34.31 |
| **Greed** | 50,303 | 38.48% | $5,736.88 | $42.74 |
| **Extreme Greed** | 39,992 | 46.49% | $3,112.25 | $67.89 |

### Core Discoveries:
1. **The Extreme Greed Profit-Taking Engine:** Traders achieve their highest efficiency during *Extreme Greed* (Win Rate: 46.49%, Avg PnL: $67.89), while downsizing position sizes to protect capital. Direct **Sell** orders net an average of **$290.57** (92.43% win rate).
2. **Strategic Scaling During Fear:** Capital allocation peaks during *Fear* ($7,816.11 average size), indicating heavy dip-buying and short-covering windows where **Close Short** actions net an average of **$207.68**.
3. **The Panic Flipping Trap:** Position flipping (Short > Long) during *Extreme Fear* is highly destructive, yielding an average loss of **-$1,932.52 per trade**.

## 🚀 Trading Strategy Recommendations
* **Anti-Euphoria Rule:** Reduce target position sizes by 40-50% during *Extreme Greed* to minimize drawdown risks before a market reversal.
* **Dip-Buying Allocation:** Scale up position exposure during *Fear* phases to capitalize on structurally discounted pricing.
* **Execution Filter:** Restrict intra-day directional flipping during high-volatility liquidations (*Extreme Fear*).

## 🛠️ Project Structure
* `Hyperliquid_Sentiment_Analysis.ipynb`: Main Jupyter Notebook containing data cleaning, merging, and exploratory data analysis (EDA).
* `sentiment_performance.png`: Visualized performance trends across sentiment categories.
