# GIS Methodology

## 1. Software and Coordinate Reference System

- Software: QGIS
- Coordinate Reference System: NZTM2000 (EPSG:2193)
- Study area: Tauranga Harbour, Bay of Plenty, New Zealand

## 2. Data Preparation

Historical seagrass habitat polygons were obtained from the Tauranga Localised Datasets 1943–1960, provided through the New Zealand Department of Conservation (DOC).

The 1948 and 1960 survey records were extracted into separate vector layers for comparison.

## 3. Geometry Validation

The extracted polygon layers were inspected for invalid geometries.

Invalid geometries were corrected using QGIS geometry validation and repair tools before spatial overlay operations.

## 4. Area Calculation

Polygon areas were calculated in hectares using the projected coordinate reference system.

The calculated area values were stored in a dedicated attribute field.

## 5. Spatial Overlay Analysis

The QGIS Intersection tool was used to identify the spatial overlap between the 1948 and 1960 seagrass polygons.

The resulting intersection layer represents the mapped area common to both survey periods.

## 6. Classification of Spatial Change

The mapped habitat was classified into three categories:

- **Persistent seagrass:** Area mapped in both 1948 and 1960.
- **Mapped loss:** Area mapped in 1948 but not in 1960.
- **Mapped expansion:** Area mapped in 1960 but not in 1948.

## 7. Statistical Analysis

Area statistics were calculated for each survey year and spatial-change category.

Persistence percentages were calculated relative to the mapped area in each survey year.

## 8. Map Production

A QGIS print layout was created to communicate the spatial distribution of persistent habitat, mapped loss and mapped expansion.

The final map includes a title, legend, north arrow, scale bar, area statistics, data source and coordinate reference system.

## 9. Reproducibility Note

The analysis describes changes in mapped seagrass extent between historical survey periods. Differences in survey methods, spatial accuracy and mapping coverage should be considered when interpreting the results.
