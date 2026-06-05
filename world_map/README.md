# World Countries Boundaries

This folder contains the shapefile representing the boundaries of all countries worldwide. The dataset is used to generate the project atlases and map visualizations, providing the administrative country polygons used as a geographic reference layer.

## Data Source

The dataset originates from the **Natural Earth** project:

https://www.naturalearthdata.com/

Natural Earth is a public domain map dataset that provides high quality vector and raster geographic data for cartographic production and GIS applications. It is one of the most widely used sources for global basemaps and administrative boundaries. The dataset includes country boundaries for approximately 247 countries and territories worldwide. :contentReference[oaicite:0]{index=0}

## Available Resolutions

Natural Earth data are freely available and can be downloaded at different spatial resolutions depending on the intended use:

* **1:10m** – High resolution
* **1:50m** – Medium resolution
* **1:110m** – Small scale / global overview

Users may choose the resolution that best fits their requirements. Higher resolutions provide more detailed geometries but result in larger file sizes.

## Local Installation

Download the desired country boundaries dataset from the Natural Earth website and extract the archive into this folder.

The extracted shapefile should contain all standard shapefile components, for example:

```text
ne_50m_admin_0_countries.shp
ne_50m_admin_0_countries.shx
ne_50m_admin_0_countries.dbf
ne_50m_admin_0_countries.prj
...
```

All shapefile components must remain together in the same directory.

## License

Natural Earth datasets are distributed as public domain data and can be freely downloaded, modified, and redistributed. Users should refer to the Natural Earth website for the latest dataset versions and documentation.
