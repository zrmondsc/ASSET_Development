# ⚡ Renewable Energy Resource Assessment and Connectivity Modelling - Continental US Scale ⚡

## Project Overview
This project has three phases. In `Phase 1: Resource Assessment` we develop a spatially explicit model of utility scale solar and onshore wind installations across the CONUS. In `Phase 2: Area Analysis` we assess the distribution of our model, and compare them to a similar dataset by Wu et al. (2023). `Phase 3: Transmission Modelling` models electrical connectivity for renewable resources and transmission lines and electric substations at various voltage classes. 

## Project Highlights
We can add some flashy visualizations here

## ☀️ Phase 1: Resource Assessment  
This repository contains (1) Jupyter Notebooks used to perform a continental scale site suitability assessment for wind and solar resources and (2) visualizations of outputs. 

#### Methodology and Code
We developed our model for site suitability by closely following the method outlined by Wu et al. (2023). The main steps in our analysis are described below:

1. [createEnvironmentalExclusion.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/createEnvironmentalExclusion.ipynb): Create environmental exclusion layer  comprising land area across United States that has legal protection against renewable energy development. A complete list of all geospatial datasets used for this analysis can be found [here](https://github.com/zrmondsc/ASSET_Development/blob/master/SupplementaryTables/EnvironmentalExclusionDatasets.xlsx).
2. [createTechnicalInclusionAreas.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/createTechnicalInclusionAreas.ipynb): Create technical inclusion layer based on various techno-economic criteria for renewable siting. A list of the datasets used in this analysis and an explanation of the different criteria for **solar** and **wind** can be found [here](https://github.com/zrmondsc/ASSET_Development/blob/master/SupplementaryTables/TechnoEconomicInclusionDatasets.xlsx). 
3. [createThresholdRasters.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/createThresholdRasters.ipynb): Create technical *exclusion* layer based on various techno-economic criteria for renewable siting. A list of the datasets used in this analysis and an explanation of the different criteria for **solar** and **wind** can be found [here](https://github.com/zrmondsc/ASSET_Development/blob/master/SupplementaryTables/TechnoEconomicExclusionDatasets.xlsx).
4. [maskInclusionRaster.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/maskInclusionRaster.ipynb): Create inclusion area layer representing land area across the US that is suitable for utility scale **solar** or **wind** development. This layer is created using a raster based approach. We subtract the outputs of (1) and (3) from (2). The inclusion layer is converted to a vectorfor further processing and subsequent analysis. 

## 🤓 Phase 2: Area Analysis 
### Methodology and Code

## 🌐 Phase 3: Transmission Modelling 
### Methodology and Code

## Figures and Visualizations

## Requirements

  
