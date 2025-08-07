# Binance MACD Strategy (Analysis Only)

A simple Python tool to analyze buy/sell crossover signals using the MACD indicator for cryptocurrency pairs on Binance.

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Optionally set Binance API keys (not required for public klines):

```bash
export BINANCE_API_KEY=your_key
export BINANCE_API_SECRET=your_secret
```

## Usage

Analyze default symbols with 4h candles:

```bash
python binance_macd_strategy.py
```

Specify symbols and interval:

```bash
python binance_macd_strategy.py --symbols BTCUSDT,ETHUSDT,BNBUSDT --interval 1h
```

Backfill more than 1000 candles by paginating (may take longer):

```bash
python binance_macd_strategy.py --symbols BTCUSDT --interval 1h --auto-fetch --lookback-days 180
```

Discover and analyze top 10 USDT symbols by 24h quote volume:

```bash
python binance_macd_strategy.py --discover --quote USDT --top-n 10 --interval 4h
```

Disable colored output:

```bash
python binance_macd_strategy.py --no-ansi
```

This tool is for research and educational purposes only. No trading advice.
