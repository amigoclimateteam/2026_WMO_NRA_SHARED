# Chile Administrative Boundaries

This folder contains the administrative boundary shapefiles for Chile used in this project.

## Data Source

Unlike the global country boundaries used elsewhere in the project, the Chilean administrative boundaries were **not derived from the Natural Earth dataset**.

The shapefiles contained in this folder were provided directly by the project stakeholders during **Phase 1** of the project and therefore represent the official reference dataset agreed upon for all analyses and atlas production related to Chile.

The dataset is distributed under the name:

```text
REGIONES_v1
```

and contains the geometry of the Chilean territory and its administrative regions.

## Important Note

Although Chile is also included in the global country boundaries dataset downloaded from Natural Earth, the project exclusively uses the **REGIONES_v1** dataset for Chile.

This choice ensures consistency with the geographical reference data supplied by the project stakeholders and guarantees that all maps, statistics, and atlas products are generated using the same official geometry adopted during Phase 1.

For this reason, the Chilean boundaries extracted from Natural Earth should **not** be used as a replacement for the files contained in this folder.

## Local Installation

Place all shapefile components belonging to the **REGIONES_v1** dataset inside this directory.

The folder should contain files similar to:

```text
REGIONES_v1.shp
REGIONES_v1.shx
REGIONES_v1.dbf
REGIONES_v1.prj
...
```

All shapefile components must remain together in the same directory.

## Usage

The geometries contained in this dataset are used for:

* Chile-specific atlas generation
* Regional aggregation of indicators
* Administrative boundary visualization
* Spatial analyses performed within the project

Any workflow involving Chilean administrative regions should use the **REGIONES_v1** dataset stored in this folder.
