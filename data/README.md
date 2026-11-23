# Data Documentation

## 1. Study Area

**Tauranga Harbour, Bay of Plenty, New Zealand**

This project examines historical seagrass (*Zostera muelleri*) distribution within Tauranga Harbour using spatial datasets from three survey years.

## 2. Primary Data Source

- **Dataset:** Tauranga Localised Datasets 1943–1960
- **Provider:** New Zealand Department of Conservation (DOC)
- **Original compilation:** Primarily regional council datasets, with contributions from DOC and other agencies.
- **Data format:** Historical seagrass habitat polygons.

The dataset was accessed through the DOC-hosted ArcGIS MapServer service.

## 3. Survey Years and Feature Counts

| Survey year | Number of features |
|---|---:|
| 1943 | 39 |
| 1948 | 89 |
| 1960 | 78 |
| **Total** | **206** |

## 4. Coordinate Reference System

- **CRS:** NZTM2000
- **EPSG code:** 2193

All spatial overlay and area calculations were conducted using this projected coordinate reference system.

## 5. Data Processing

The following processing steps were carried out in QGIS:

1. Extraction of individual survey years from the original dataset.
2. Geometry validation and correction using the Fix Geometries tool.
3. Calculation of polygon areas in hectares.
4. Spatial intersection to identify overlapping mapped seagrass areas.
5. Difference analysis to identify mapped loss and mapped expansion.
6. Classification and visualisation of persistent mapped habitat, mapped loss and mapped expansion.

## 6. Important Data Limitations

The mapped extents represent historical survey records rather than continuous ecological observations.

Differences in survey methods, mapping scale, positional accuracy and spatial coverage may influence comparisons between survey years.

Therefore, the results should be interpreted as changes in mapped seagrass extent rather than definitive evidence of ecological loss, recovery or expansion.

## 7. Software

- QGIS – spatial data processing, analysis and cartographic visualisation.
