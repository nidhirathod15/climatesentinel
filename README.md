# climatesentinel
# Sentinel-1 Flood Detection – Assam Floods 2024
## Overview
This project demonstrates how satellite radar data can be used to detect flood-affected areas. Using Sentinel-1 Synthetic Aperture Radar (SAR) imagery and Google Earth Engine, the project analyzes flooding in the Dibrugarh–Majuli region of Assam during the 2024 flood season. The main idea is to compare satellite images taken **before** and **during** the flood and identify areas where land suddenly appears like water in radar data. The workflow produces a flood mask and estimates the total flooded area.

## Why SAR Data
Optical satellite images often fail during disasters because clouds block the view. Sentinel-1 uses radar, which can see through clouds and operate day or night. This makes it useful for monitoring floods during heavy monsoon conditions.

## Method
1. **Region Selection**
   A region of interest was defined over the Dibrugarh–Majuli area of Assam.
2. **Data Collection**
   Sentinel-1 SAR imagery was retrieved from Google Earth Engine for two time periods:
   * Pre-flood: May 2024
   * Post-flood: June 2024
3. **Change Detection**
   The radar backscatter values from the two time periods were compared. When land becomes flooded, the radar signal drops. A ratio threshold was used to detect these changes and generate a flood mask.
4. **Flood Area Calculation**
   Pixel area analysis was used to estimate the total flooded region within the study area.

## Result
Detected Flood Area: **223,831 hectares**
Equivalent Area: **2,238 km²**
The generated flood mask highlights areas likely affected by flooding during the peak of the Assam floods in June 2024.

## Tools and Technologies
- Python
- Google Earth Engine
- Geemap
- Sentinel-1 SAR Satellite Data

## Possible Improvements
This workflow can be extended by:
* Using multiple time periods to track flood progression
* Combining SAR data with optical imagery
* Applying machine learning methods for improved flood classification
* Automating the system for near real-time flood monitoring

