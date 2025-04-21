# Ursus Americanus: Spatial Statistics
This project investigates the spatial patterns of black bear (*Ursus americanus*) occurrences using environmental covariates. The goal is to model the relationship between bear sightings and four key spatial variables: elevation, HFI (Human Footprint Index), distance to water, and forest cover. The analysis is conducted using spatial statistical methods in R.

## Project Overview
This project explores how environmental variables broken out into the seasons influence bear occurrences in British Columbia, Canada. We use spatial statistical techniques in R to analyze the relationships between bear locations and four covariates:

- Elevation: Altitude of different areas
- Human Footprint Index (HFI): Measure of human influence on landscape
- Distance to Water: Proximity to water bodies
- Forest Cover: Percentage of forested area

The analysis incorporates spatial dependencies between the observations, providing insights into spatial autocorrelation and patterns.

### Installation
Several R packages are required to run this project - please use `install.packages()` function in R. The key packages needed are as follows:

- `sp`: Handling spatial data 
- `sf`: Handling spatial vector data
- `spatstat`: Analysis of spatial point patterns
- `rgbif`: Accessing data from the Global Biodiversity Information Facility (GBIF) to work with species occurrence data
- `ggplot2`: Data visualization and plotting
- `tidyverse`: Collection of packages for data manipulation, visualization, and analysis
- `raster`: Working with raster data 

## Data

Black bear occurrences were sourced from the Global Biodiversity Information Facility (GBIF) for the past 5 years (2020 - 2024). Covariate data, including the spatial window, were provided by the UBC MDS program.

## Methodology

### Data Preprocessing

- Occurrence records were filtered by species, location (British Columbia), and observation date (2020–2024).
- All spatial layers were reprojected to a common coordinate reference system (BC Albers).
- NA values in raster covariates (e.g., forest cover) were imputed using mean values within the study region.
- Bear observations were split by season (spring, summer, autumn, winter) and converted into spatial point pattern objects (ppp class).

### Exploratory Analysis

- Mapped black bear occurrences in British Columbia from 2020–2024 as spatial point patterns using projected coordinates.
- Filtered and grouped bear sightings by season (spring, summer, autumn, winter) to create seasonal point pattern datasets.
- Applied kernel density estimation (KDE) to visualize intensity surfaces for each season.
- Conducted quadrat tests using a 5x5 grid to assess deviations from spatial randomness in seasonal patterns.

### Model Fitting

- Fitted inhomogeneous Poisson point process models (PPMs), starting with univariate models for each covariate to assess individual associations.
- Combined covariates in a multivariate model, incorporating both linear and quadratic terms where appropriate to account for potential nonlinear relationships.
- Developed season-specific models to evaluate how environmental associations vary across spring, summer, autumn, and winter.
- Also fitted a marked point process model treating season as a categorical mark, allowing direct comparison of intensity surfaces across seasons.
- Evaluated model performance using Akaike Information Criterion (AIC) and diagnostic plots based on smoothed partial residuals.

### Acknowledgements
We would like to acknowledge the contributions from various sources:

- `R` Community: For providing open-source packages that were essential for the analysis and visualization in this project.
- Global Biodiversity Information Facility (GBIF): For offering valuable species occurrence data, which enabled analysis on Ursus americanus.

### Contributors  

## Contributors
- [![Vidal Tinoco](https://github.com/VidalTinoco.png?)](https://github.com/VidalTinoco) — @VidalTinoco  
- [![Kelsey Strachan](https://github.com/kstrachan556.png?)](https://github.com/kstrachan556) — @kstrachan556
- [![Jane Shen](https://github.com/j232shen.png?)](https://github.com/j232shen) — @j232shen
- [![Amali Jayatileke](https://github.com/ajayatil.png?)](https://github.com/ajayatil) — @ajayatil  

## License
This project is licensed under the MIT License.
