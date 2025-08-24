Machine Learning Adaptive SuperTrend [AlgoAlpha] (with Alerts)

This repository contains a modified version of the Machine Learning Adaptive SuperTrend indicator originally created by AlgoAlpha.

The base script combines the classic SuperTrend with a K-Means clustering algorithm that adapts ATR values to volatility regimes (high / medium / low).
My primary contribution is the addition of real-time alerts tied to the indicator’s trading signals, making it actionable within TradingView’s alerting system.

✨ What’s New in This Version

🔔 Alerts Added (my contribution):

alert() calls fire whenever ▲ (Bullish Trend Shift) or ▼ (Bearish Trend Shift) markers plot.

Alert messages include ticker, timeframe, close price, current volatility cluster, and ATR centroid.

Configurable under TradingView’s Any alert() function call.

💡 Impact: With this update, traders can now receive push notifications, emails, or webhook events the moment a strategy signal occurs — even without watching the chart.

📊 Features (Base Indicator by AlgoAlpha)

Adaptive SuperTrend: ATR dynamically adjusted by K-Means clustering of recent volatility.

Volatility Regimes:

Cluster 3 → High volatility

Cluster 2 → Medium volatility

Cluster 1 → Low volatility

Chart Visuals:

▲ Bullish Trend Shift markers

▼ Bearish Trend Shift markers

On-chart table showing cluster centroids, cluster sizes, and current ATR level

⚙️ Inputs

ATR Length: Length for ATR calculation

SuperTrend Factor: ATR multiplier for bands

Training Data Length: Lookback for K-Means clustering

Initial High/Medium/Low Percentiles: Starting cluster guesses

Appearance: Colors, transparency for bullish/bearish bands

🔔 Alerts

Supported alert events include:

Bullish Trend Shift (▲)

Bearish Trend Shift (▼)

High Volatility Detected

Medium Volatility Detected

Low Volatility Detected

Sample Alert Message:

▲ Bullish Trend Shift on AAPL (1h) @ 192.45 | Vol Cluster=MEDIUM | ATR centroid=1.25

🖥️ Usage

Add this Pine Script to the TradingView Pine Editor.

Save and add to chart.

Configure inputs if desired.

Create an Alert in TradingView:

Condition: this indicator

Trigger: Any alert() function call

Delivery: App push, email, webhook, or SMS

📌 Acknowledgments

Original script authored by AlgoAlpha.

Alerts functionality added by [Your Name].

⚠️ Disclaimer

This script is for educational purposes only. It is not financial advice.
Use at your own risk. Always backtest and paper trade before using in live markets.
