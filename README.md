# Heikin-Ashi Momentum Stacking Strategy

Systematic trend-following strategy using Heikin-Ashi structure.

Built with Pine Script v6 for quantitative momentum research.

Includes pyramiding, regime filtering, and adaptive exits.


A systematic long/short algorithmic trading strategy built in **Pine Script v6**, designed to capture persistent market trends using Heikin-Ashi price structure, momentum continuation logic, and volatility-normalized risk management.

---

## 📌 Project Overview

This project converts discretionary Heikin-Ashi chart analysis into a fully rule-based quantitative trading model.  
The strategy focuses on identifying strong directional momentum, scaling into trends through pyramiding, and exiting positions using early reversal and trend-fatigue signals.

The objective is to create a robust trend-following system that performs well in volatility-clustered market regimes while minimizing exposure during sideways conditions.

---

## 🧠 Core Strategy Logic

### 1️⃣ Trend & Momentum Detection
- Custom Heikin-Ashi candle computation for noise reduction.
- Strong bullish/bearish candle classification using body-to-shadow structure.
- Momentum confirmation via **K consecutive strong candles**.
- Early breakout entry when abnormal candle expansion occurs.

### 2️⃣ Entry Logic
- Standard momentum entry after consecutive strong directional candles.
- Additional entry trigger:
  - Three small-bodied candles with near-equal wicks (compression pattern)
  - Entry in direction of prevailing trend.
- Supports **long and short entries simultaneously**.
- Position pyramiding enabled for trend stacking.

### 3️⃣ Exit Logic
- Exit on strong reversal-colored candle indicating momentum shift.
- Trend fatigue detection:
  - Consecutive small, wick-dominant reversal candles.
  - Early exit before full trend breakdown.

### 4️⃣ Risk Management
- ATR-based volatility-normalized stop-loss.
- Anti-chop filter to avoid low-volatility sideways markets.
- Controlled pyramiding for exposure scaling.

---

## 📊 Backtest Summary

| Metric | Value |
|--------|-------|
| Timeframe | 1H / 4H |
| Markets Tested | BTCUSDT, ETHUSDT, Index CFDs |
| Win Rate | ~XX% |
| Max Drawdown | ~XX% |
| Sharpe Ratio | ~X.X |
| Profit Factor | ~X.X |

> Note: Performance varies across market regimes and is strongest during sustained trends.

---

## 🧪 Key Concepts Applied

- Trend-following momentum models
- Volatility clustering
- Position pyramiding
- Regime filtering (anti-chop logic)
- Structural price-action formalization

---

## 📷 Example Results

*(Add screenshots here)*

- Equity curve
- Trade distribution
- Strategy tester statistics

---

## 🚀 Future Improvements

- Adaptive momentum threshold based on volatility regime
- Dynamic pyramiding limits
- Live execution via exchange API (OKX/Binance)
- Portfolio-level risk allocation

---

## ⚠️ Disclaimer

This project is for research and educational purposes only.  
It is not financial advice and should not be used for live trading without further validation.

---

## 👤 Author

Neel — AI & Data Science | Quantitative Trading Enthusiast
