# 📈 Stock Watchlist Monitor

A lightweight Python script to monitor your stock watchlist in real-time using Yahoo Finance — no heavy libraries required.

## Features

- **Real-time prices** — fetches live stock prices from Yahoo Finance
- **USD/IDR conversion** — automatically fetches the latest exchange rate
- **Change alerts** — notifies when a stock moves more than 3% from previous close
- **Auto-refresh** — updates every 60 seconds
- **Clean terminal display** — compact and readable layout

## Watchlist (example)

| Ticker | Company |
|--------|---------|
| AAPL | Apple |
| MU | Micron Technology |
| STX | Seagate Technology |
| PLTR | Palantir |
| ASML | ASML |
| MSFT | Microsoft |
| IONQ | IonQ Inc |
| NVDA | NVIDIA |
| GOOGL | Google |
| AMZN | Amazon |
| AVGO | Broadcom |

## Installation

No external dependencies beyond the standard `requests` library:

```bash
pip install requests
```

## Usage

```bash
python watchlist_saham.py
```

Press `Ctrl+C` to stop.

## Sample Output

```
  ================================
  WATCHLIST SAHAM
  27/04/2026 22:10:00
  Kurs: Rp16.200
  ================================
  AAPL  Apple
  $172.50    Rp2.795.100      ▲ +1.23%
  --------------------------------
  NVDA  NVIDIA
  $880.00    Rp14.256.000     ▼ -3.45%  ⚠ TURUN
  ================================

  ⚠ ALERT (>= 3.0%):
  • NVDA TURUN -3.45%

  Refresh dalam 60s... (Ctrl+C stop)
```

## Configuration

Edit these variables at the top of the script to customize:

```python
ALERT_THRESHOLD_PERCENT = 3.0   # Alert if stock moves more than this %
REFRESH_INTERVAL = 60            # Refresh every N seconds
WATCHLIST = { ... }              # Add or remove your stocks here
```

## Tech Stack

- `requests` — HTTP calls to Yahoo Finance API
- No `yfinance`, no `pandas` — minimal dependencies

## License

MIT
