# Station Data

This directory is intended to store the meteorological station data provided by each project partner for the atlas generation workflows.

## Folder Structure

Create a subdirectory named after your country using **lowercase letters only**.

Examples:

```text
station_data/
├── chile/
├── peru/
├── ecuador/
├── colombia/
└── bolivia/
```

Place all station datasets shared for this project inside the corresponding country folder.

## Data Source

The files stored in these directories should be the original station datasets provided by the project partners and national institutions during the data collection phase.

The format may vary from country to country depending on the source and delivery method.

## Processing Workflow

The station datasets contained in the country folders are used as input for the **station data preprocessing and cleaning notebook**.

The notebook automatically:

* Reads the original station files.
* Performs quality control and data cleaning.
* Standardizes variable names and formats.
* Handles missing or inconsistent records where possible.
* Aggregates observations to monthly values.
* Produces a harmonized output dataset ready for spatial interpolation.

The final output is a standardized CSV file containing cleaned and monthly aggregated station observations.

## Output

After processing, the notebook generates a standardized CSV file with:

* Station metadata.
* Geographic coordinates.
* Monthly aggregated climate variables.
* Consistent formatting across all countries.

These CSV files are subsequently used as input for the **Inverse Distance Weighting (IDW)** interpolation workflow.

## Important Note

Please keep the original station datasets unchanged inside the country folder. All cleaning, formatting, and aggregation operations are performed automatically by the preprocessing notebook, which generates separate standardized outputs for downstream analyses.

## Notes for Argentina

Due to the format in which the station data were shared, the folder structure for Argentina differs slightly from the standard layout.

Inside the `argentina` directory, create one subfolder for each station and place the corresponding Excel files for that station inside its dedicated folder.

The expected structure is:

```text
station_data/
└── argentina/
    ├── Ushuaia/
    ├── Tucumán/
    ├── Rio_Gallegos/
    ├── Pilar/
    ├── Neuquén/
    ├── Mendoza/
    ├── La_Quiaca/
    ├── Comodoro_Rivadavia/
    ├── Buenos_Aires/
    └── Bariloche/
```

The station folders to be created are:

* Ushuaia
* Tucumán
* Rio_Gallegos
* Pilar
* Neuquén
* Mendoza
* La_Quiaca
* Comodoro_Rivadavia
* Buenos_Aires
* Bariloche

Each folder should contain all Excel files associated with the corresponding station.

The preprocessing notebook has been configured to automatically scan these station-specific directories, process the original files, and generate the standardized monthly CSV outputs required for the subsequent IDW interpolation workflow.

## Notes for Peru

Due to the format in which the Peruvian station data were shared, some preprocessing steps were performed before integrating the datasets into the project workflow.

For each station, the information contained in the **"Resumen"** worksheet was extracted and consolidated into a dedicated file:

```text
resumen_estaciones_peru.xlsx
```

This file contains the station metadata and summary information required by the preprocessing workflow.

Similarly, station coordinates were extracted, converted to decimal degrees where necessary, and collected in the dedicated file:

```text
stations_coordinates_decimal.csv
```

The preprocessing notebook uses these two files as the primary source of station metadata and geographic coordinates for Peru.

Please ensure that both files are available within the `peru` directory before running the preprocessing workflow.
