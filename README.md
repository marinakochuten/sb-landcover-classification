# Landcover classification with a decision tree in R

![landcover classification map](https://github.com/marinakochuten/sb-landcover-classification/blob/main/figs/sb-landcover-map.png?raw=true)

## About

Monitoring the distribution and change in land cover types can help us understand the impacts of phenomena like climate change, natural disasters, deforestation, and urbanization. Determining land cover types over large areas is a major application of remote sensing because we are able to distinguish different materials based on their spectral reflectance.

Classifying remotely sensed imagery into land cover classes enables us to understand the distribution and change in land cover types over large areas.

There are many approaches for performing land cover classification:

- **Supervised** approaches use training data labeled by the user
- **Unsupervised** approaches use algorithms to create groups which are identified by the user afterward

In this analysis, I am using a form of supervised classification – a decision tree classifier - to create a land cover classification for southern Santa Barbara County based on multi-spectral imagery and data on the location of 4 land cover types:

- green vegetation
- dry grass or soil
- urban
- water

## Highlights

- Load and process Landsat data
- Crop and mask Landsat data to study area
- Extract spectral data at training sites
- Train and apply decision tree classifier
- Plot results

## Repository contents

There are 3 subdirectories within my repository:
-  `docs/` folder contains the code files for my analysis
    - `landcover_classification.qmd` is the quarto file for my analysis
    - `landcover_classification.html` is the rendered version of the .qmd file
    - `landcover_classification_files/` contains the associted files for the rendered .html file
- `data/` folder contains all of the data files used in my analysis - see data details for more info on these files
- `figs/` folder contains the final output of my analysis - a landcover classification map for Santa Barbara

## Data details

#### Landsat 5 Thematic Mapper

- Landsat 5
- 1 scene from September 25, 2007
- Bands: 1, 2, 3, 4, 5, 7
- Collection 2 surface reflectance product

**Data files:**

- `landsat-data/LT05_L2SP_042036_20070925_20200829_02_T1_SR_B1.tif`
- `landsat-data/LT05_L2SP_042036_20070925_20200829_02_T1_SR_B2.tif`
- `landsat-data/LT05_L2SP_042036_20070925_20200829_02_T1_SR_B3.tif`
- `landsat-data/LT05_L2SP_042036_20070925_20200829_02_T1_SR_B4.tif`
- `landsat-data/LT05_L2SP_042036_20070925_20200829_02_T1_SR_B5.tif`
- `landsat-data/LT05_L2SP_042036_20070925_20200829_02_T1_SR_B7.tif`

#### Study area

Polygon representing southern Santa Barbara county

**Data file:** `SB_county_south.shp`

#### Training data

Polygons representing sites with training data - *type:* character string with land cover type

**Data file:** `trainingdata.shp`

## Acknowledgements

This repository was created as an assignment for the graduate course EDS 223: Geospatial Analysis and Remote Sensing in the [Masters of Environmental Data Science (MEDS) program](https://bren.ucsb.edu/masters-programs/master-environmental-data-science), taught by [Dr. Ruth Oliver](https://bren.ucsb.edu/people/ruth-oliver).


