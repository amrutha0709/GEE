# Fire Impact Analysis using Earth Engine

## Description
This script analyzes fire-affected areas in Brazil using satellite imagery and vegetation indices. It calculates the pre- and post-fire conditions, evaluates changes, and classifies burned areas based on NDVI (Normalized Difference Vegetation Index).

## Key Features
- **Study Area**: Focused on Brazil, using FAO's GAUL dataset for boundaries.
- **Data Sources**: 
  - Fire data from MODIS (`MCD12Q1`).
  - Pre- and post-fire imagery from Sentinel-2 (`COPERNICUS/S2`).
- **Indices**: Calculates NDVI and its delta to assess vegetation loss.
- **Classification**: Identifies burned areas using NDVI thresholds.
- **Validation**: Compares NDVI-based classification with official fire classifications.

## Steps in the Script
1. **Data Preparation**:
   - Filter and clean fire data based on valid dates and study area.
   - Retrieve Sentinel-2 images for pre- and post-fire periods.
2. **Processing**:
   - Calculate NDVI for pre- and post-fire images.
   - Compute delta NDVI to assess vegetation changes.
3. **Classification**:
   - Identify burned and unburned areas using a threshold (-0.23).
   - Mask invalid or non-fire zones.
4. **Visualization**:
   - Visualize pre-fire NDVI, post-fire NDVI, delta NDVI, and classifications.
5. **Accuracy and Results**:
   - Reports non-vegetative area and classification accuracy.

## Outputs
- **Maps**:
  - NDVI before and after the fire.
  - NDVI change (delta).
  - Burn classification map.
- **Metrics**:
  - Non-vegetative area post-fire: **3,392,300 km²**.
  - Percentage of non-vegetative area: **39.83%**.
  - Accuracy rate: **97.89%**.

## Usage
Run the script in Google Earth Engine to analyze fire impacts, classify affected areas, and validate the results. Adjust parameters like `threshold` or `delta` for custom analyses.

---
