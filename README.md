Climate and Vegetation Monitoring for Chad (July–September 2022) <br>

This script analyzes and visualizes precipitation, soil moisture, and vegetation indices (NDVI & EVI) for Chad over a three-month period (July–September 2022). The data is processed and aggregated at both country (admin level 0) and province/state (admin level 1) levels using Google Earth Engine (GEE).

🧭 Objectives <br>

Retrieve and process climate and vegetation data for Chad.
Compute average values for precipitation, soil moisture, NDVI, and EVI.
Produce tables summarizing these indicators by administrative region.
Visualize spatial patterns on an interactive map.

🗂️ Sections <br>
1. Data Sources <br>
Variable	Source	Dataset ID <br>
Elevation	USGS	USGS/SRTMGL1_003 <br>
Precipitation	CHIRPS	UCSB-CHG/CHIRPS/DAILY <br>
Soil Moisture	SMAP	NASA/SMAP/SPL4SMGP/007 <br>
Vegetation Index	MODIS	MODIS/006/MOD13A2 <br>

2. Timeframe <br>
Start Month: July 2022 <br>
End Month: September 2022 <br>
Chosen to capture the peak of the main agricultural season in Chad. <br>

3. Data Processing <br>
🔸 Precipitation <br>
Aggregated from CHIRPS daily data. <br>
Computed as sum over 3 months for each region. <br>
🔸 Soil Moisture <br>
Extracted from SMAP surface moisture data. <br>
Calculated as a mean value across the time period. <br>
🔸 Vegetation Indices <br>
NDVI & EVI derived from MODIS. <br>
Values averaged across July–September. <br>
Rescaled by multiplying by 0.0001 (as MODIS returns scaled integers). <br>

4. Outputs<br>
An interactive 🗺️ geemap.Map() displaying: <br>
Precipitation (CHIRPS, summed) <br>
Soil Moisture (SMAP, averaged) <br>
NDVI (MODIS, averaged) <br>
All layers are clipped to Chad’s Admin1 boundaries and color-coded. <br>
