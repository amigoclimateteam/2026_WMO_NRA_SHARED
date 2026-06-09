# HydroRIVERS Data

This project uses river network data from the **HydroRIVERS** dataset, developed by **HydroSHEDS**.

HydroRIVERS is a globally consistent vector database of river networks derived from HydroSHEDS hydrographic data. It provides river reaches represented as line features and includes attributes such as river order, reach length, upstream drainage area, estimated discharge, and connectivity information. The dataset is widely used for hydrological modelling, river network analysis, climate impact assessments, and water resource studies.

## Downloading the Data

Download the HydroRIVERS dataset from the official HydroSHEDS website:

https://www.hydrosheds.org/products/hydrorivers

For this project, download the **South America (SA)** shapefile dataset. 
The downloaded archive is typically named:

```text
HydroRIVERS_v10_sa_shp.zip
```

After downloading, extract the archive.

## Dataset Contents

HydroRIVERS contains river reaches represented as vector line features. Rivers are extracted from HydroSHEDS and include all river segments with a catchment area of at least 10 km² or an average discharge of at least 0.1 m³/s. Each river reach includes several useful attributes describing the river network topology and geometry. 

Some commonly used attributes include:

* River ID
* River order
* Upstream drainage area
* Reach length
* Distance to outlet
* Estimated discharge
* Connectivity to upstream and downstream reaches

## Local Installation

The HydroRIVERS dataset is distributed as a ZIP archive.

Download the South America dataset from the HydroSHEDS website:

```text
HydroRIVERS_v10_sa_shp.zip
```

After downloading:

1. Create a local directory named exactly as the ZIP file (without the `.zip` extension):

```text
HydroRIVERS_v10_sa_shp
```

2. Extract all contents of the ZIP archive into this directory.

The resulting structure should look similar to:

```text
data/
└── HydroRIVERS_v10_sa_shp/
    ├── HydroRIVERS_v10_sa.shp
    ├── HydroRIVERS_v10_sa.shx
    ├── HydroRIVERS_v10_sa.dbf
    ├── HydroRIVERS_v10_sa.prj
    ├── HydroRIVERS_v10_sa.cpg
    ├── ...
```

All shapefile components must remain together in the same directory. Do not rename individual files, as project scripts may expect the original HydroRIVERS file names.

## GitHub Storage Notice

HydroRIVERS files can be relatively large and are therefore not included in this repository.

Users must download the dataset directly from HydroSHEDS and place the extracted files in the local directory described above before running any scripts or workflows that depend on river network data.

Please ensure that the `HydroRIVERS_v10_sa_shp` directory exists locally and contains all files extracted from the original HydroSHEDS ZIP archive before running the project workflows.
