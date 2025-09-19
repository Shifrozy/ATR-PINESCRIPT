# ATR Trailing Stop Strategy (Pine Script v6)

![TradingView Logo](https://cdn.iconscout.com/icon/free/png-256/tradingview-2832968-2355374.png)

## 📖 Description
This repository contains a TradingView **Pine Script v6 strategy** that implements a **volatility‑based trailing stop** using the Average True Range (ATR).  

- 🟢 **Long trades:** Exit when price drops **N × ATR** below the highest close since entry.  
- 🔴 **Short trades:** Exit when price rises **N × ATR** above the lowest close since entry.  
- 📊 Plots all tracking lines directly on the candlestick chart for easy visualization.  
- 🔔 Supports TradingView alerts via `alertcondition()` for precise notifications.  
- ⚡ Includes sample entry logic (10/30 SMA crossover) which you can replace with your own strategy.  

---

## ✨ Features
- ✅ Works for both **longs and shorts** (mirrored ATR trailing logic).  
- ✅ **Overlay mode** → plots on candlesticks instead of a separate pane.  
- ✅ Built‑in **alerts** for automated notifications.  
- ✅ Clean, modular code with clear sections for entries, exits, tracking, and alerts.  
- ✅ Includes full backtesting support with TradingView Strategy Tester.  

---

## ⚙️ Inputs
| Input          | Description                                  | Default |
|----------------|----------------------------------------------|---------|
| ATR Length     | ATR smoothing length                         | 14      |
| ATR Multiple   | Multiplier for trailing distance             | 3.0     |
| Enable Longs   | Toggle long trades                           | true    |
| Enable Shorts  | Toggle short trades                          | true    |

---

## 🔔 Alerts Setup in TradingView
1. Copy the script into the **Pine Script editor** and add to your chart.  
2. Open the **Alerts (⏰)** panel.  
3. Select the script under *Condition*.  
4. Choose:
   - **Exit Long (ATR Trail)**  
   - **Exit Short (ATR Trail)**  
   … depending on which alert you want.  
5. Choose your delivery method (popup, app notification, email, webhook).  
6. Click **Create**.  

Optional: Select “Any alert() function call” to capture all alerts at once.  

---

## 📊 Visualizations
The script plots the following directly on your candlestick chart:  

- 🟢 **Green line** → highest close since long entry  
- 🟣 **Purple line** → lowest close since short entry  
- 🔴 **Red line** → ATR trailing stop for longs  
- 🔵 **Blue line** → ATR trailing stop for shorts  

---

## ▶️ Example Entry Logic
This repo uses a **10/30 SMA crossover** purely for demonstration:
- **Long entry:** when 10‑SMA crosses above 30‑SMA  
- **Short entry:** when 10‑SMA crosses below 30‑SMA  

🔧 Replace this section with your own strategy entries — the ATR trailing logic will adapt automatically.  

---

