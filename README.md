# PV Performance Analysis – Dortmund

## Project Overview
This project analyzes the solar photovoltaic (PV) potential in Dortmund, Germany using PVGIS hourly solar radiation data (2015–2023). The goal is to calculate PV energy output, visualize trends, and explore advanced features like tilt optimization or economic payback.

## Folder Structure
- data/       : Raw PVGIS CSV files
- notebooks/  : Jupyter notebooks for analysis
- results/    : Plots, charts, and reports
- README.md   : Project description and progress

## Assumptions
- PV panel area: 1 m²  
- Panel efficiency: 18% (typical for standard solar panels)  
- Energy calculation is hourly, based on Global Irradiance (G(i)) from PVGIS  
- Units:  
  - Irradiance → W/m²  
  - PV energy → Wh  
- Rounding applied for readability in portfolio dataset

## Daily Progress

### Day 1 – Setup & Data Exploration
- Project folders created (data/, notebooks/, results/)
- PVGIS data downloaded for Dortmund
- CSV data loaded and cleaned using pandas
- Time column converted to datetime
- Numeric columns converted to float
- Initial plot of Global Irradiance created


### Day 2 – Data Cleaning & Hourly PV Energy
- Cleaned column names and reordered columns  
- Calculated hourly PV energy (Wh) with panel assumptions  
- Rounded numeric values for portfolio readability  
- Exported clean CSV and optional Excel  
-“Hourly PV energy was calculated for each row (hourly timestep). Annual totals were aggregated and plotted as a bar chart.”


### Day 3 – Daily and Monthly PV Energy Analysis
- Set `time` column as the DataFrame index to enable time-series resampling
- Aggregated hourly PV energy (`PV_Energy_Wh`) into **daily PV energy production**
- Converted daily energy values from **Wh to kWh**
- Generated a **daily PV energy production plot** to observe short-term solar variability
- Aggregated daily energy values into **monthly PV energy production**
- Calculated the **average monthly PV energy output (2015–2023)** to analyze seasonal solar patterns
- Created a **monthly average PV energy bar chart** showing seasonal production trends
- Exported processed datasets to the `results/` folder (`daily_energy.csv`, `monthly_energy.csv`)

**Observation:**  
The results show a clear seasonal PV generation pattern in Dortmund, with **highest energy production during summer months (June–July)** and **lowest production during winter months (December–January)** due to reduced solar irradiation and shorter daylight hours.


### Day 4 – PV Visualization Analysis
- Reloaded the cleaned PV dataset and ensured the `time` column was set as the DataFrame index for time-based analysis
- Extracted the **hour of day** from the timestamp to analyze typical daily PV production behavior
- Calculated the **average hourly PV energy output** across the entire dataset (2015–2023)
- Created a **Daily PV Production Curve** showing how solar generation varies during a typical day
- Calculated **annual PV energy production** by aggregating hourly PV energy values for each year
- Converted the annual results into a bar chart to compare **year-to-year PV production**
- Extracted the **month value** from the timestamp to analyze seasonal solar behavior
- Constructed a **pivot table (month vs hour)** to compute the average PV production for each month-hour combination
- Created a **Solar Production Heatmap** visualizing how PV energy generation changes throughout the day and across seasons

**Observation:**
- Solar energy production peaks around **midday hours (11:00–14:00)** due to maximum solar irradiance.
- **Summer months (May–August)** show the highest PV production due to longer daylight duration and higher solar angles.
- **Winter months (November–January)** show significantly lower PV generation due to shorter daylight hours and lower solar irradiation levels.

**Outputs generated (saved in `results/` folder):**
- `daily_production_curve.png`
- `annual_energy_plot.png`
- `solar_heatmap.png`