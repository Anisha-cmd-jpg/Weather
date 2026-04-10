# Live Weather Dashboard

A live weather dashboard built with **Streamlit** and **Plotly**, powered by the free [Open-Meteo API](https://open-meteo.com) — no API key required.

---

## Features

- Current conditions: temperature, humidity, wind speed, visibility, pressure, weather condition
- Temperature anomaly detection (flags if current temp deviates >5°C from 5-day average)
- 5-day interactive charts: temperature trend, humidity, wind speed
- Celsius / Fahrenheit toggle
- Auto-refresh (every 30 or 60 minutes) via `streamlit-autorefresh`
- Manual refresh button
- Raw forecast data table (expandable)

---

## Project Structure

```
weather_dashboard/
├── weather_dashboard.py   # Main app file
├── requirements.txt       # Python dependencies
└── README.md              # This file
```

---

## Setup & Installation

### 1. Prerequisites

- Python 3.8 or higher
- pip

### 2. Clone or download

Place `weather_dashboard.py` and `requirements.txt` in the same folder.

### 3. (Recommended) Create a virtual environment

```bash
python -m venv venv

# Activate on macOS/Linux:
source venv/bin/activate

# Activate on Windows:
venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Run the app

```bash
streamlit run weather_dashboard.py
```

The app will open automatically in your browser at `http://localhost:8501`.

---

## Dependencies

| Package | Purpose |
|---|---|
| `streamlit` | Web app framework |
| `requests` | HTTP calls to Open-Meteo & geocoding APIs |
| `pandas` | Hourly forecast data processing |
| `plotly` | Interactive charts |
| `streamlit-autorefresh` | Auto-refresh the dashboard on a timer |

---

## APIs Used

| API | URL | Key required? |
|---|---|---|
| Open-Meteo Forecast | `https://api.open-meteo.com/v1/forecast` | No |
| Open-Meteo Geocoding | `https://geocoding-api.open-meteo.com/v1/search` | No |

---

## Usage

1. Enter a city name in the sidebar (default: Coimbatore)
2. Choose temperature unit (Celsius or Fahrenheit)
3. Select auto-refresh interval (30 or 60 minutes)
4. Click **Refresh Now** to manually reload data

---

## Troubleshooting

| Issue | Fix |
|---|---|
| City not found | Try a more specific name, e.g. "Chennai, India" |
| Auto-refresh not working | Run `pip install streamlit-autorefresh` and restart |
| Timeout errors | Check your internet connection |
| Charts not rendering | Ensure `plotly` is installed correctly |
