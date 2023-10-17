# Solar and On Shore Wind Suitability Assessement - Continental US Scale
This repository contains (1) Jupyter Notebooks used to perform a continental scale site suitability assessment for wind and solar resources (2) Data tables and supporting information enumerating geospatial resources used for each analysis and (3) Visualizations of outputs. 

## Methodology and Code
We developed our model for site suitability by closely following the method outlined by Wu et al. (2023). The main steps in our analysis are described below:

1. [createEnvironmentalExclusion.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/createEnvironmentalExculsion.ipynb): Create environmental exclusion layer  comprising land area across United States that has legal protection against renewable energy development. A complete list of all geospatial datasets used for this analysis can be found [here](https://github.com/zrmondsc/ASSET_Development/blob/master/SupplementaryTables/EnvironmentalExclusionDatasets.xlsx). 
2. [createTechnicalInclusionAreas.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/createTechnicalInclusionAreas.ipynb): Create technical inclusion layer based on various techno-economic criteria for renewable siting. A list of the different criteria for **solar** and **wind** can be found [here](link). A list of datasets used for this analysis can be found [here]([link](https://github.com/zrmondsc/ASSET_Development/blob/master/SupplementaryTables/TechnoEconomicInclusionDatasets.xlsx)). 
3. [createThresholdRasters.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/createThresholdRasters.ipynb): Create technical *exclusion* layers based on various techno-economic criteria for renewable siting. A list of the different criteria for **solar** and **wind** can be found [here](link). A list of datasets used for this analysis can be found [here]([link](https://github.com/zrmondsc/ASSET_Development/blob/master/SupplementaryTables/TechnoEconomicExclusionDatasets.xlsx)).
4. [maskInclusionRaster.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/maskInclusionRaster.ipynb): Create inclusion area layer representing land area across the US that is suitable for utility scale **solar** or **wind** development. This layer is created using a raster based approach. We subtract the outputs of (1) and (3) from (2). The inclusion layer is converted to a vector and clipped to the shape of the CONUS for further processing and analysis. 

## Figures and Visualizations

## Requirements

  
