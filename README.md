# Bitcoin Trader Sentiment Analysis

**Analyzing the impact of Bitcoin market sentiment on Hyperliquid trader performance**

---

##  Overview

This project explores the relationship between Bitcoin market sentiment (using the Fear/Greed Index) and the trading performance of users on the Hyperliquid platform. The analysis focuses on how market sentiment influences trader profitability, position sizing, trading volume, and provides actionable insights for developing smarter trading strategies.

---

##  Objectives

- **Combine Bitcoin market sentiment data** (Fear/Greed Index) with historical trader data from Hyperliquid.
- **Analyze trader performance** (profit/loss, trade volume, position size) across different sentiment categories.
- **Identify patterns and correlations** between market sentiment and trader behavior.
- **Develop and evaluate trading strategies** based on sentiment extremes.

---

##  Data Sources

- **Bitcoin Market Sentiment Dataset**
  - **Columns:** `timestamp`, `value`, `classification` (Fear/Greed), `date`
- **Hyperliquid Trader Data**
  - **Columns:** `Account`, `Coin`, `Execution Price`, `Size Tokens`, `Size USD`, `Side`, `Timestamp IST`, `Start Position`, `Direction`, `Closed PnL`, `Transaction Hash`, `Order ID`, `Crossed`, `Fee`, `Trade ID`, `Timestamp`

---

## Methodology

1. **Data Preprocessing**
   - Load and clean the sentiment and trader datasets.
   - Convert timestamps and extract relevant date features.
   - Merge datasets on the common date field.

2. **Feature Engineering**
   - Calculate daily trader performance metrics:
     - **Total Profit/Loss (PnL)**
     - **Trade Count**
     - **Total Trading Volume (USD)**
     - **Average Position Size (Tokens)**

3. **Sentiment-Performance Analysis**
   - Group trader performance by sentiment category.
   - Visualize PnL, trading volume, and position size distributions across sentiment levels.
   - Perform statistical tests to compare performance during fear vs. greed periods.

4. **Strategy Development**
   - Develop a contrarian trading strategy:
     - **Long positions during Extreme Fear periods**
     - **Short positions during Extreme Greed periods**
   - Propose sentiment-based risk management rules (leverage, position sizing, stop-loss).

---

##  Key Findings

- **Higher Trading Volume During Fear:** Traders are more active during fear-driven markets, but use smaller position sizes.
- **Larger Positions During Greed:** Traders take larger positions during greed periods, but trading volume decreases.
- **Profitability:** No statistically significant difference in average PnL between fear and greed periods, but extreme sentiment periods show distinct behavioral patterns.
- **Contrarian Strategy:** Shorting during Extreme Greed and buying during Extreme Fear outperforms a neutral strategy.
- **Risk Management:** Sentiment extremes signal opportunities for adjusting leverage and position sizing to manage risk.

---

##  Sample Visualizations

- **PnL Distribution by Market Sentiment:** Boxplots showing profit/loss across sentiment categories.
- **Average Daily Trading Volume by Sentiment:** Bar charts comparing trading volume.
- **Sentiment vs. Trader Performance Over Time:** Time-series plots of sentiment index and average PnL.

---
