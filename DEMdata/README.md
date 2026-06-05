# Orography and Terrain Data

This folder contains the datasets required to generate the terrain-derived variables used throughout the atlas production workflow, including **elevation (orography)** and **aspect**.

## ERA5-Land Geopotential

The first dataset required is the **ERA5-Land geopotential**, a global, time-invariant land parameter provided by ECMWF as part of the ERA5-Land dataset.

The geopotential field represents the geopotential value at the terrain surface and is provided at a spatial resolution of 0.1° × 0.1°.

Additional documentation is available at:

https://confluence.ecmwf.int/display/CKB/ERA5-Land%3A+data+documentation

The dataset can be downloaded directly from:

https://confluence.ecmwf.int/download/attachments/140385202/geo_1279l4_0.1x0.1.grib2_v4_unpack.nc?version=1&modificationDate=1591983422003&api=v2

Place the downloaded NetCDF file inside this directory.

### Why Is It Needed?

The ERA5-Land geopotential is used as the starting point for deriving terrain characteristics.

The workflow converts geopotential into **orography (terrain elevation)** by dividing the geopotential values by the gravitational acceleration (9.81 m/s²):

```text
Elevation = Geopotential / 9.81
```

The resulting elevation model is then used to derive:

* Orography (terrain elevation)
* Terrain aspect
* Additional topographic predictors used by the atlas methodology

## Copernicus DEM GLO-90

In addition to the ERA5-Land geopotential, the workflow requires the **Copernicus DEM GLO-90** dataset.

The Copernicus DEM GLO-90 is a global Digital Elevation Model with approximately 90 m spatial resolution and is used to provide detailed terrain information for each country.

Documentation and download information are available through the Copernicus Data Space Ecosystem.

## Country-Specific Folders

Create one subdirectory for each country using lowercase names:

```text
orography_data/
├── argentina/
├── bolivia/
├── chile/
├── colombia/
├── ecuador/
├── peru/
└── ...
```

Within each country folder, download and place all Copernicus DEM GLO-90 tiles required to fully cover the national territory.

Example:

```text
orography_data/
├── argentina/
│   ├── Copernicus_DSM_90m_...
│   ├── Copernicus_DSM_90m_...
│   └── ...
│
├── chile/
│   ├── Copernicus_DSM_90m_...
│   └── ...
```

## Processing Workflow

The terrain preprocessing notebook automatically:

* Reads the ERA5-Land geopotential dataset.
* Computes the terrain elevation (orography).
* Merges and processes the Copernicus DEM tiles for each country.
* Derives terrain aspect and related topographic variables.
* Produces standardized outputs used by the atlas generation workflow.

## Notes

The required input datasets are not included in this repository due to their size.

Before running the terrain preprocessing workflow, ensure that:

* The ERA5-Land geopotential NetCDF file is available in this directory.
* A country-specific folder exists for each target country.
* The corresponding Copernicus DEM GLO-90 tiles have been downloaded and placed inside the appropriate country folder.
