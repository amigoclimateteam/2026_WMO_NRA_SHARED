# HydroBASINS Data

This project uses watershed boundaries from the **HydroBASINS** dataset, developed by **HydroSHEDS**. HydroBASINS is a globally consistent database of nested watershed and sub-basin boundaries derived from high-resolution digital elevation models. It is widely used for hydrological modelling, water resource management, environmental assessments, and climate impact studies.

## Downloading the Data

Download the HydroBASINS dataset from the official HydroSHEDS website:

https://www.hydrosheds.org/products/hydrobasins

For this project, download the **South America (SA)** HydroBASINS dataset.

## HydroBASINS Levels

HydroBASINS provides a hierarchical subdivision of river basins based on the Pfafstetter coding system. Lower levels represent larger drainage areas, while higher levels provide increasingly detailed watershed subdivisions.

| Level | Description |
|---------|---------|
| 1 | Continental-scale drainage regions |
| 3 | Major river basins |
| 5 | Medium-scale sub-basins |
| 7 | Smaller sub-basins |
| 10 | Local watershed units |
| 12 | Highest available spatial resolution |

Each level is nested within the previous one, allowing analyses at multiple spatial scales.

## Levels Used in This Project

This project uses:

* **Level 5** for regional-scale analyses.
* **Level 12** for maximum watershed detail and local-scale analyses.

## Local Installation

After downloading and extracting the South America HydroBASINS archive, copy the shapefile components into the appropriate local project directory.

Each HydroBASINS level is distributed as a shapefile consisting of multiple files that must remain together:

* `.shp`
* `.shx`
* `.dbf`
* `.prj`
* `.cpg`
* `.sbn`
* `.sbx`

Typically, there are **7 files per level**, all of which are required for proper use.

Example structure:

```text
data/
└── hydrobasins/
    ├── level_5/
    │   ├── hybas_sa_lev05_v1c.shp
    │   ├── hybas_sa_lev05_v1c.shx
    │   ├── ...
    │
    └── level_12/
        ├── hybas_sa_lev12_v1c.shp
        ├── hybas_sa_lev12_v1c.shx
        ├── ...
```

## GitHub Storage Notice

HydroBASINS files can be relatively large and may exceed GitHub storage recommendations or repository limits. For this reason, the shapefiles are **not included in this repository**.

Users must download the data directly from HydroSHEDS and place the extracted files in the local directories described above before running any scripts or workflows that depend on watershed boundaries.

Please ensure that both **Level 5** and **Level 12** datasets are available locally before executing the project.
