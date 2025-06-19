# Python-PowerBI

# ORB Strategy Backtesting and Analysis

This repository contains a two-part project that implements and analyzes an **Opening Range Breakout (ORB)** trading strategy using Python and Power BI. The goal is to backtest the strategy on intraday stock data and visualize the performance with meaningful financial KPIs and charts.

## 📌 Project Overview

### Project 1: Python – Backtest ORB Strategy

**Objective:**  
Backtest an Opening Range Breakout (ORB) strategy on intraday 5-minute data for multiple stocks.

**Strategy Rules:**
- Identify the **first 5-minute candle** of each trading day.
- **Buy Entry:** If price crosses **above the high** of the first candle, enter a **long** position.
- **Sell Entry:** If price crosses **below the low** of the first candle, enter a **short** position.
- Only one **buy** and one **sell** trade allowed per symbol per day.

**Risk-Reward Conditions:**
- **Target:** +0.5%
- **Stop Loss:** -0.25%
- **Exit Time:** 15:15 (if SL/target not hit)

**Output:**  
A detailed trade log with:
- Date, Symbol, Entry/Exit Time
- Entry/Exit Price, PnL
- Exit Reason (Target/SL/Time)
  
📄 The trade log output is saved in CSV format for use in Power BI.

---

### Project 2: Power BI – Analyze ORB Strategy Performance

**Objective:**  
Visualize the ORB strategy’s performance using calculated KPIs and charts in Power BI.

**Data Source:**  
Trade log CSV generated from Python script.

**Calculated Fields:**
- Trade Count per Day
- Weekday of Trade
- Cumulative PnL
- Drawdown from peak
- Holding Duration (in minutes)
- Entry Hour

**KPIs (Cards):**
- ✅ Total PnL  
- 🔢 Total Trades  
- 🟢 Win Count (PnL > 0)  
- 🔴 Loss Count (PnL < 0)  
- 📉 Maximum Drawdown  
- 📊 Average Drawdown  
- 💡 Expectancy (Avg PnL per trade)  
- 📏 Calmar Ratio (Total PnL / Max Drawdown)  
- 📈 Average Win PnL  
- 📉 Average Loss PnL  
- ⚖️ Win/Loss Ratio  
- 🏅 Longest Win Streak  
- 💥 Longest Loss Streak  

**Visualizations:**
1. 📈 Cumulative PnL Line Chart  
2. 📉 Drawdown Line Chart  
3. 🥧 Win vs Loss Pie Chart  
4. 📊 Month-wise PnL Bar Chart  
5. 📆 Weekday-wise PnL Bar Chart  
6. ⏰ Hourly PnL Heatmap  
7. 🧾 Exit Reason PnL Pie Chart  
8. ⏳ Trade Duration Distribution  
9. 🏆 Top 5 Winning Trades  
10. 🚨 Top 5 Losing Trades  

---

## 📜 License

This project is for educational and personal use only. Not intended as financial advice or for real trading use.
