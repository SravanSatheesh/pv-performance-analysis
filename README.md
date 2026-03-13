# PV Performance Analysis – Dortmund, Germany

## Project Overview

This project evaluates the photovoltaic (PV) energy generation potential in Dortmund, Germany using long-term hourly solar irradiation data obtained from PVGIS for the period 2015–2023.

The objective is to perform data-driven PV performance modelling, visualize solar energy production patterns, and assess the technical and economic feasibility of residential PV installations.

---

## Project Objectives

* Analyse long-term solar resource availability
* Model photovoltaic energy production using irradiance data
* Study seasonal and daily PV performance trends
* Evaluate impact of panel tilt angle on annual energy yield
* Estimate economic payback period for a residential PV system

Tools used: **Python (pandas, numpy, matplotlib), Jupyter Notebook**

---

## Folder Structure

* `data/` → Raw and processed PVGIS datasets
* `notebooks/` → Jupyter notebooks containing analysis workflow
* `results/` → Generated plots, processed tables, and technical report
* `README.md` → Project description and methodology

---

## Modelling Assumptions

* PV panel area: **1.6 m²**
* Module efficiency: **18%** (typical crystalline silicon module performance)
* PV energy calculated hourly using Global Irradiance G(i)
* Units used:

  * Irradiance → W/m²
  * Energy → Wh and kWh
* Simplified tilt correction factors used for sensitivity analysis
* Economic evaluation based on average German residential electricity price

---

## Methodology

### Data Processing

* PVGIS hourly solar irradiation dataset imported and cleaned
* Time column converted to datetime format
* Numeric parameters converted to floating-point values
* Hourly PV energy output calculated from irradiance

### Energy Aggregation

* Hourly PV energy aggregated into:

  * Daily production
  * Monthly average production
  * Annual energy generation

### Visual Analysis

The following visualisations were generated:

* Daily PV production curve (typical diurnal pattern)
* Monthly average PV generation bar chart (seasonal trend)
* Annual energy comparison plot
* Solar production heatmap (month vs hour distribution)
* Tilt angle sensitivity comparison chart

---

## Economic Evaluation

A simplified economic analysis was conducted assuming a small residential PV installation.

* Estimated annual PV electricity production used to calculate potential savings
* Installation cost assumptions applied
* Simple payback period estimated based on electricity price

---

## Key Findings

* PV generation in Dortmund shows strong **seasonal variability**
* **Summer months contribute the highest solar energy yield** due to longer daylight duration and higher solar angles
* **Peak daily generation occurs around midday (11:00–14:00)**
* Panel tilt angle of approximately **30° provides optimal annual energy output**
* Residential PV systems demonstrate **reasonable cost recovery potential** under current electricity pricing

---

## Conclusion

The analysis demonstrates that rooftop photovoltaic systems are technically viable and economically beneficial for residential applications in Dortmund.

The project highlights the importance of solar resource assessment, system orientation, and performance modelling in renewable energy planning.

This workflow illustrates how Python-based data analysis can support informed decision-making in solar energy engineering.

---

## Project Status

Completed as a self-driven renewable energy data analysis portfolio project.
