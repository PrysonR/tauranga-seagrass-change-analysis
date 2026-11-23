# GIS Methodology

## 1. Software and Coordinate Reference System

- **Software:** QGIS
- **Coordinate Reference System:** NZTM2000 (EPSG:2193)
- **Study Area:** Tauranga Harbour, Bay of Plenty, New Zealand

The projected coordinate reference system was used to support spatial overlay operations and area calculations.

## 2. Data Preparation

Historical seagrass habitat polygons were obtained from the Tauranga Localised Datasets 1943–1960, provided through the New Zealand Department of Conservation (DOC).

The 1948 and 1960 survey records were extracted into separate vector layers for comparison.

The original dataset also contained records from 1943, but the spatial change-detection analysis documented in this project focuses on the 1948–1960 period.

## 3. Geometry Validation

The extracted polygon layers were inspected for invalid geometries before spatial analysis.

The QGIS **Fix Geometries** tool was used to repair invalid geometries in the 1948 and 1960 datasets.

The corrected layers were used in subsequent spatial overlay operations.

## 4. Area Calculation

Polygon areas were calculated using the projected coordinate reference system (EPSG:2193).

The QGIS field calculator was used to convert polygon areas from square metres to hectares.

**Calculation:**

`$area / 10000`

The calculated values were stored in a dedicated attribute field named `Area_ha_calc`.

## 5. Spatial Overlay Analysis

Spatial overlay operations were conducted to compare the mapped seagrass extents between 1948 and 1960.

Two main operations were performed:

- **Intersection:** Identified areas mapped as seagrass in both survey periods. These areas were classified as persistent mapped seagrass.
- **Difference (1948 minus 1960):** Identified areas mapped in 1948 but not in 1960, classified as mapped loss.
- **Difference (1960 minus 1948):** Identified areas mapped in 1960 but not in 1948, classified as mapped expansion.

These operations were used to identify spatial overlap and differences between the two historical datasets.

## 6. Classification of Spatial Change

The results were classified into three categories:

- **Persistent Seagrass:** Areas mapped in both 1948 and 1960.
- **Mapped Loss:** Areas mapped in 1948 but not in 1960.
- **Mapped Expansion:** Areas mapped in 1960 but not in 1948.

These categories describe differences in mapped spatial extent and do not independently establish ecological survival, loss or recovery.

## 7. Statistical Analysis

Area statistics were calculated for each survey year and spatial-change category.

The total mapped area for each survey period was calculated by summing the `Area_ha_calc` field.

Persistence percentages were calculated using the intersection area relative to the total mapped area in each survey period.

**Percentage overlap in 1948:**

`(Intersection area / Total mapped area in 1948) × 100`

**Percentage overlap in 1960:**

`(Intersection area / Total mapped area in 1960) × 100`

## 8. Map Production

A QGIS print layout was created to communicate the spatial distribution of persistent mapped habitat, mapped loss and mapped expansion.

The final map includes:

- Map title
- Legend
- North arrow
- Scale bar
- Area statistics
- Data source information
- Coordinate reference system

## 9. Reproducibility and Limitations

The analysis was conducted using QGIS and the historical seagrass polygon datasets described in the data documentation.

The results represent changes in mapped seagrass extent between historical survey periods.

Differences in survey methods, mapping scale, positional accuracy and spatial coverage may influence the results. Spatial overlap should not be interpreted as proof of continuous ecological survival, and mapped expansion should not automatically be interpreted as ecological recovery.
