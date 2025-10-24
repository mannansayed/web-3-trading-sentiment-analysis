# web-3-trading-sentiment-analysis
Data Science assignment analyzing the relationship between trader performance and Bitcoin market sentiment (Fear vs Greed) using Hyperliquid trade data.


# Web3 Trading Team – Sentiment vs Trader Performance Analysis

This repository contains a data science project exploring how trader performance metrics relate to Bitcoin market sentiment (Fear vs Greed).  
The analysis was completed as part of the **Web3 Trading Team Data Science assignment** by **Mannan Sayed** on **8 October 2025**.

---

## 📊 Project Overview
The objective of this analysis is to uncover patterns between **market sentiment** and **trader outcomes**, and evaluate whether trading behavior aligns with periods of Fear or Greed in the market.

---

## 🧠 Datasets Used
1. **Bitcoin Market Sentiment Dataset**
   - Columns: `Date`, `Classification (Fear/Greed)`, `Value`
   - Source: Historical Fear & Greed Index

2. **Hyperliquid Trader Data**
   - Columns: `Account`, `Coin`, `Execution Price`, `Size USD`, `Side`, `Closed PnL`, `Leverage`, `Timestamp`, etc.

---

## ⚙️ Data Processing & Methodology
- Parsed and merged both datasets by `Date`.
- Aggregated trade-level data into **daily metrics**:
  - Total volume (USD)
  - Average & median PnL
  - Win rate (fraction of profitable trades)
  - Trade count
- Merged with daily sentiment (Fear/Greed + numeric index value).
- Conducted statistical comparison and exploratory plots.

---

## 📈 Visualizations
- **Time-Series Plot:** Daily average PnL vs. scaled sentiment value  
- **Boxplot:** Distribution of average PnL during Fear vs Greed periods  
- **Correlation Matrix:** Interrelations between numeric features  
- **ROC Curve:** Preliminary logistic model for predicting profitable days

---

## 🧩 Key Findings
- Sample size too small for reliable hypothesis testing (only 3 valid daily points).  
- Early trends suggest that trader profitability tends to vary between Fear and Greed periods.  
- Larger data windows and feature-rich modeling are required for robust insights.

---

## 🚀 Future Improvements
- Include more historical trade data (30+ days).  
- Add BTC price, volatility, and rolling indicators.  
- Use time-series and non-linear ML models for improved prediction.

---

## 🗂️ Repository Structure
ds_mannan_sayed/
├── csv_files/
│ ├── hyperliquid_trades.csv
│ └── fear_greed.csv
├── outputs/
│ ├── timeseries_avgpnl_sentiment.png
│ ├── box_avgpnl_by_sentiment.png
│ ├── corr_matrix.png
│ └── roc_curve.png
├── notebook_1.ipynb
├── daily_merged_mannan.csv
└── Mannan_Sayed_ds_report_8-10-2025.pdf
