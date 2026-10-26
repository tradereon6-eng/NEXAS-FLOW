# MMT Flow — Live Order Flow Terminal

A GitHub Pages-ready, read-only crypto market dashboard with live Binance Spot data.

## Features
- Live price and 24-hour ticker stats
- Candlestick chart with 1m, 5m, 15m, and 1h intervals
- Live top-of-book depth snapshot (top 10 asks and bids displayed)
- Live trades feed
- Live footprint approximation aggregated from Binance `aggTrade` events for the current minute
- BTC, ETH, SOL, BNB, XRP USDT markets
- Responsive dark interface

## Run locally
Open `index.html` in a modern browser, or use VS Code Live Server. Internet access is required.

## Publish with GitHub Pages
1. Create a GitHub repository, e.g. `mmt-flow`.
2. Upload `index.html` and this README.
3. In repository settings, open **Pages**.
4. Choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
5. Wait for the published URL shown in the Pages section.

## Data notes
- Uses Binance public Spot REST and WebSocket endpoints; no API key is needed.
- A network, browser extension, regional restriction, or exchange outage can block live data.
- The footprint is calculated from trades received after connection. It does not include historical bid/ask footprint data.
- Binance `aggTrade` maker flag is used to infer aggressor side: buyer-is-maker = sell aggressor; otherwise buy aggressor.
- The DOM is a displayed top-of-book depth snapshot stream, not a full exchange order-book reconstruction.
- This project does not place orders, hold funds, connect to accounts, or request API secrets.
- It is an analytics interface, not financial advice.
