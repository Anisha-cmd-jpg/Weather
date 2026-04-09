# 🌤️ Live Weather Dashboard

A real-time weather dashboard built with Streamlit, Plotly, and Open-Meteo API — no API key required.

## Features

- 📍 Search any city worldwide
- 🌡️ Current conditions — temperature, feels like, humidity, wind, pressure, visibility
- ⚠️ Temperature anomaly detection (flags deviation > 5° from 5-day average)
- 📈 5-day hourly forecast charts — temperature, humidity, wind speed
- 🔄 Auto-refresh every 30 or 60 minutes
- °C / °F toggle

## Requirements

- Python 3.8+

## Installation

```bash
pip install streamlit requests pandas plotly streamlit-autorefresh
```

## Usage

```bash
streamlit run WEATHER.py
```

Then open [http://localhost:8501](http://localhost:8501) in your browser.

## Deployment (Streamlit Community Cloud)

1. Push your code to a GitHub repository
2. Go to [streamlit.io/cloud](https://streamlit.io/cloud) and sign in
3. Click **New app** → select your repo and file
4. Click **Deploy** — you'll get a free public URL

## Data Source

[Open-Meteo](https://open-meteo.com) — free, open-source weather API, no API key needed.

## Tech Stack

| Library | Purpose |
|---|---|
| Streamlit | Web UI framework |
| Plotly | Interactive charts |
| Pandas | Data manipulation |
| Requests | API calls |
| streamlit-autorefresh | Auto-refresh support |
| Open-Meteo | Weather & geocoding API |
