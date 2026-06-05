# IRI Wind Climatology Data

This folder contains the wind climatology datasets used for the generation of wind maps and indicators within the project atlases.

The data originate from the **IRI Data Library**, maintained by the International Research Institute for Climate and Society (IRI):

https://iridl.ldeo.columbia.edu/

The same climatological wind datasets are also used in the regional climate products available through the CIIFEN Climate Regional Atlas:

https://crc-osa.ciifen.org/

## Dataset Description

The datasets provide monthly climatological wind fields derived from the **NOAA NCEP/NCAR CDAS-1 Reanalysis** and distributed through the IRI Global Climatologies portal.

The wind climatology is represented by two variables:

* **U wind component** (zonal wind, east-west direction)
* **V wind component** (meridional wind, north-south direction)

These variables can be combined to derive wind speed and direction and are used to produce the wind maps included in the atlas products.

## Data Source

The original datasets are available through the IRI Global Climatologies portal:

https://iridl.ldeo.columbia.edu/maproom/Global/Climatologies/Vector_Winds.html

The data are provided as monthly climatological averages and can be downloaded in NetCDF format directly from the IRI Data Library.

## Local Installation

Download the required NetCDF files from the IRI Data Library and place them in this folder.

The project expects both climatological wind components to be available:

```text
u.nc
v.nc
```

(or equivalent filenames containing the U and V wind climatologies).

## Usage in the Project

These datasets are used to:

* Generate climatological wind maps for the atlases.
* Compute wind speed and direction fields.
* Support regional climate characterization across South America.
* Provide the wind layers displayed in the CIIFEN Climate Regional Atlas products.
