# RainCheck: Geospatial Data Integration for Urban Climate Risk Intelligence

RainCheck is a geospatial research prototype exploring how environmental and population datasets can be integrated to compare relative urban climate stress across Mumbai wards.

## Project objective

Urban areas experience climate pressures such as extreme heat and flooding. RainCheck explores a ward-level framework for combining geospatial indicators and population exposure to support more spatially informed climate-risk assessment.

## Current status

**Completed component:** Ward-level heat-stress mapping prototype.

**Study area:** Mumbai, India.

**Analysis unit:** 24 ward records.

## Methodology

The workflow uses GIS and raster analysis to summarise environmental datasets across ward boundaries.

The current heat-stress index combines three equally weighted indicators:

- Normalised land-surface temperature
- Vegetation stress, derived from inverse-normalised NDVI
- Normalised population exposure

The selected indicators are normalised to a common scale and combined into a composite score. The resulting map uses five quantile classes to visualise relative differences within the analysed sample.

## Results

The current heat-stress scores range from 0.196 to 0.865 across the 24 analysed ward records.

These values are relative index scores, not absolute measures of danger or validated predictions of health impacts.

## Map output

See the [Mumbai heat-stress map (PDF)](outputs/RainCheck_Heat_Stress_Mumbai_June2026_QAchecked.pdf).

## Tools and datasets

- QGIS for spatial processing and map production
- Google Earth Engine for satellite-data access and processing
- MODIS land-surface temperature and vegetation-index products
- SRTM elevation data
- CHIRPS precipitation data
- WorldPop population estimates, using a 2020 baseline

Dataset dates, resolutions, source links and processing decisions should be documented in the methodology and data-source records.

## Limitations

- The analysis uses 24 ward records.
- Datasets differ in spatial resolution and reference period.
- The index uses exploratory equal weighting.
- The population dataset uses a 2020 baseline.
- Independent validation has not been completed.
- Flood-stress modelling is not yet complete.
- RainCheck is a research prototype, not a fully operational urban digital twin.

## Future directions

Possible extensions include flood-stress assessment, sensitivity testing, independent validation, improved temporal coverage, and integration of multiple climate hazards.

## Reproducibility

The repository documents the workflow and outputs. Reproducibility depends on the availability of the source datasets and the inclusion of the relevant processing scripts.

## Author

Jagriti  
BSc Data Science, NMIMS, Mumbai
