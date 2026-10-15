# FasalAlert — Crop Stress & Weather Risk Advisory Dashboard

**Group:** SpatioFarm
**Members:** K. Yaswanthi, Swathi A Patil, Sathvik, Himanshu
**Course:** MSc Agriculture Analytics — Python Project 2026

---

## What is FasalAlert?

FasalAlert is a crop stress advisory dashboard that:

* Fetches weather data for Indian districts.
* Computes a Crop Stress Score (CSS) based on weather anomalies.
* Displays results on an interactive pan-India choropleth map.
* Issues actionable advisories for districts experiencing crop stress.

---

## Tech Stack

* **GUI:** Streamlit
* **Geospatial:** GeoPandas, Folium, Shapely
* **API:** OpenWeatherMap (Requests)
* **Data:** IMD Climate Normals, ICAR Crop Calendar, GADM District Boundaries

---

## How to Run

### Step 1 — Install dependencies

```bash
pip install -r requirements.txt
```

### Step 2 — Launch the application

```bash
python main.py
```

---

## Folder Structure

```text
fasal_alert/
├── data/                        # GeoJSON, CSV, and JSON data files
├── docs/                        # Project reports and documentation
├── src/
│   ├── gui/
│   │   └── app.py               # Dashboard interface
│   ├── logic/
│   │   ├── stress.py            # CSS formula and classification
│   │   └── spatial.py           # Geospatial processing and mapping
│   └── utils/
│       ├── weather_api.py       # Weather API calls
│       └── helpers.py           # Anomaly calculations and advisories
├── main.py                      # Application entry point
├── requirements.txt             # Python dependencies
├── test_geo.py                  # Geospatial tests
└── test_pipeline.py             # Pipeline tests
```

---

## Team Contributions

| Member       | Primary Role                                              |
| ------------ | --------------------------------------------------------- |
| Swathi       | `stress.py`, `crop_thresholds.json`, `crop_calendar.json` |
| Sathvik      | `app.py` — Streamlit GUI                                  |
| K. Yaswanthi | `weather_api.py` — Weather API integration                |
| Himanshu     | `spatial.py`, `helpers.py`, repository setup, README      |

---

## Demo Region

FasalAlert is designed to support districts across India, subject to the availability of the required data and weather API coverage.
