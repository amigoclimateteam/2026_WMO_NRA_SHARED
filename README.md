# WMO National Renewable Energy Atlas - Phase 3 (2026)

This repository contains a set of Jupyter Notebooks for each of the three atlases — **solar**, **wind**, and **hydropower**.  
Each notebook follows the common methodology, structured into the following steps of the workflow.

## Step-by-Step Methodology

**Step 0 — Computer setup**  
Before running the notebooks, please read the document **Computer_SetUp**.  
It provides instructions on how to install **Anaconda** (required to execute the notebooks) and how to set up the dedicated environments using the provided `.yml` files for each atlas.  

**Step 1 — Data retrieval**  
Register to the Copernicus **Climate Data Store (CDS)**, obtain the API key, install the CDS client, and script downloads for ERA5-Land and other sources as needed.  

**Step 2 — Data pre-processing**  
Apply quality control (unit harmonization, anomaly checks), temporal aggregation (e.g., daily/monthly), and derive key variables such as wind speed and direction from u/v components. For hydropower, set up the macro-basin delineation.  

**Step 3 — Downscaling**  
Apply Machine Learning–based statistical downscaling to refine ERA5-Land for solar and wind, incorporating terrain features. For hydropower, aggregate discharge within **HYDROBASINS** (Levels 5 and 12).  

**Step 4 — Data interpolation (station assimilation)**  
Interpolate in-situ observations onto the fine grid using **Inverse Distance Weighting (IDW)** to assimilate station data and enhance local representativeness.  

**Step 5 — Atlas generation**  
Merge downscaled fields with IDW maps using an uncertainty-weighted approach. Export outputs in **NetCDF** and **GeoTIFF** formats for analysis and GIS integration.  
 
**Step 6 — Visualization**  
Produce maps for:  
- **Solar**: annual/monthly Global Horizontal Irradiance (GHI)  
- **Wind**: annual/monthly speed and direction  
- **Hydro**: average discharge at national (L5) and regional (L12) levels  
Apply cartographic conventions (boundaries, rivers, gridlines, colorbars).  

**Step 7 — Climate projections**  
Extend the pipeline to **CMIP6** simulations (historical + future scenarios), compute deltas against the historical period, and apply them to ERA5/GloFAS baselines to assess future changes.

---

📂 *Notebooks are organized by atlas type (`solar/`, `wind/`, `hydro/`) and implement the methodology described above.*  

---

## Examples of output

### Hydropower NRA output example  
![Hydropower example](data/figures/tanzania_l5_hydro_annual.png)

### Wind NRA output example  
![Wind example](data/figures/cuba_wind_annual_present.png)

### Solar NRA output example   
![Solar example](data/figures/croatia_solar_annual_present.png)
