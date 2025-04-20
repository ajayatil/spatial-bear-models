# Ursus Americanus: Spatial Statistics
Project investigates the spatial patterns of bear occurrences using environmental covariates. The goal is to model the relationship between bear sightings and four key spatial variables: elevation, HFI, distance to water, and forest cover. The analysis is conducted using spatial statistical methods in R.

## Project Overview
This project explores how environmental variables broken out into the seasons influence bear occurrences in British Columbia, Canada. We use spatial statistical techniques in R to analyze the relationships between bear locations and four covariates:
- Elevation: Altitude of different areas
- Human Footprint Index (HFI): Measure of human influence on landscape
- Distance to Water: Proximity to water bodies
- Forest Cover: Percentage of forested area

The analysis incorporates spatial dependencies between the observations, providing insights into spatial autocorrelation and patterns.

### Installation
Several R packages are required to run this project - please use install.packages() function in R. The key packages needed are as follows:
- `sp`: Handling spatial data 
- `sf`: Handling spatial vector data
- `spatstat`: Analysis of spatial point patterns
- `rgbif`: Accessing data from the Global Biodiversity Information Facility (GBIF) to work with species occurrence data
- `ggplot2`: Data visualization and plotting
- `tidyverse`: Collection of packages for data manipulation, visualization, and analysis
- `raster`: Working with raster data 

## Data
[...]

## Methodology

The key steps in the analysis are:
[...]

### Data Preprocessing:

Import and clean the data.

Re-project spatial data to a common coordinate system 

### Model Fitting:

Fit spatial regression models 


## License
This project is licensed under the MIT License
