# RainCheck Methodology

## 1. Study objective

RainCheck explores how geospatial environmental and population data can be combined to compare relative urban climate stress across Mumbai wards.

## 2. Spatial unit

Ward boundaries are used as the spatial units for summarising raster datasets. The current analysis contains 24 ward records.

## 3. Data sources

| Variable | Dataset | Role |
|---|---|---|
| Land-surface temperature | MODIS MOD11A2 | Heat indicator |
| Vegetation index | MODIS MOD13A2 | Vegetation-related indicator |
| Elevation | SRTM | Terrain context for future flood analysis |
| Rainfall | CHIRPS | Rainfall context for future flood analysis |
| Population | WorldPop, 2020 baseline | Population exposure indicator |

The datasets have different spatial resolutions and reference periods. The exact date range and processing choices for each layer should be checked against the source files and analysis scripts.

## 4. Processing workflow

1. Prepare the Mumbai ward boundary layer.
2. Load and preprocess the raster datasets.
3. Mask or clip raster data to the study area where appropriate.
4. Use zonal statistics to summarise raster values within ward boundaries.
5. inspect and investigate anomalous values before using them.
6. Normalise the selected indicators to a common scale.
7. Combine the heat-related indicators into a composite index.
8. Visualise the resulting ward-level scores using quantile classification.

## 5. Heat-stress index

The current prototype combines normalised land-surface temperature, inverse-normalised NDVI, and population exposure using equal weights.

Heat Stress = (Temperature Indicator + Vegetation-Stress Indicator + Population-Exposure Indicator) / 3

Higher scores indicate higher relative stress under this index. They are not validated probabilities of heat-related harm.

## 6. Interpretation

The map uses five quantile classes. These classes describe relative differences within the analysed sample; they are not universal thresholds for safe or dangerous heat.

## 7. Limitations

- The current prototype contains 24 ward records.
- The input datasets have different spatial resolutions and dates.
- The index uses exploratory equal weights.
- The population layer uses a 2020 baseline.
- Independent validation against observed heat impacts has not been completed.
- A flood-stress index and a fully operational digital twin have not been completed.

## 8. Potential future work

Potential extensions include flood-stress assessment, sensitivity testing, validation with independent evidence, improved temporal data coverage, and integration of multiple hazards.
