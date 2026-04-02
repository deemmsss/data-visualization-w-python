# Air Quality Data Visualization

## About

This project visualizes the **Air Quality dataset** from the UCI Machine Learning Repository. The dataset contains 9,358 instances of hourly averaged sensor readings from a gas multisensor device deployed in an Italian city, recorded from March 2004 to February 2005.

**Dataset source:** [UCI Machine Learning Repository – Air Quality (ID: 360)](https://archive.ics.uci.edu/dataset/360/air+quality)

## Folder Structure

```
data-visualization-w-python/
├── air-quality-analysis.ipynb   # Main Jupyter notebook with all code and outputs
├── images/                      # Exported plot images
│   ├── line_plot_co.png
│   ├── histogram_temperature.png
│   ├── heatmap_correlation.png
│   └── scatter_temp_humidity.png
└── README.md
```

## Dataset Overview

The dataset includes hourly readings from 5 metal oxide chemical sensors along with reference measurements from a certified analyzer. Key variables include:

- **CO(GT)** – Carbon monoxide concentration (mg/m³)
- **C6H6(GT)** – Benzene concentration (µg/m³)
- **NOx(GT)** – Nitrogen oxides concentration (ppb)
- **NO2(GT)** – Nitrogen dioxide concentration (µg/m³)
- **PT08.S1–S5** – Sensor responses targeting CO, NMHC, NOx, NO2, and O3
- **T, RH, AH** – Temperature (°C), relative humidity (%), and absolute humidity

Missing values in the dataset are encoded as `-200`.

## Visualizations

Four visualizations were created to explore different aspects of the data:

1. **Line Plot** – Hourly CO concentration over time (first 500 hours), showing daily fluctuation patterns in carbon monoxide levels.
2. **Histogram** – Distribution of temperature readings across the full year, revealing a roughly normal distribution centered around 10–20°C.
3. **Correlation Heatmap** – Pairwise correlations between all numeric features, highlighting strong relationships between pollutants and sensor responses.
4. **Scatter Plot** – Temperature vs. relative humidity, showing a clear negative relationship (higher temperatures correspond to lower humidity).

## Requirements

- Python 3.10+
- pandas
- numpy
- matplotlib
- seaborn
- ucimlrepo

Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn ucimlrepo
```

## How to Run

1. Open `air-quality-analysis.ipynb` in Jupyter Notebook or JupyterLab.
2. Run all cells in order (the first cell installs `ucimlrepo` if needed).
3. Plots will display inline. Save them to `images/` if needed using `plt.savefig()`.
