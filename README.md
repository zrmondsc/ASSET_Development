# ⚡ Renewable Energy Resource Assessment and Connectivity Modelling - Continental US Scale ⚡

## Project Overview
This project has three phases. In `Phase 1: Resource Assessment` we develop a spatially explicit model of utility scale solar and onshore wind installations across the CONUS. In `Phase 2: Area Analysis` we assess the distribution of our model, and compare them to a similar dataset by Wu et al. (2023). `Phase 3: Transmission Modelling` models electrical connectivity for renewable resources and transmission lines and electric substations at various voltage classes. 

**Note:** For the spatial analyses described in this project we selected the North American Datum 1983 (NAD83) and the USA Contiguous Albers Equal Area Conic USGS Version projection. This was due to its suitability for maintaining accurate areas across the contiguous USA (**Consider switching to conformal projection for transmission modelling**). For raster based analyses, we used 250m rasters to reduce processing times for continental scale operations while maintaining moderate spatial resolution. 

## Project Highlights
We can add some flashy visualizations here

## ☀️ Phase 1: Resource Assessment  
#### Methodology and Code
We developed our model for site suitability by closely following the method outlined by Wu et al. (2023). The main steps in our analysis are described below:

1. [createEnvironmentalExclusion.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/createEnvironmentalExclusion.ipynb): Create `Environmental Exclusion Layer` comprising land area across United States that has legal protection against renewable energy development. A complete list of all geospatial datasets used for this analysis can be found [here](https://github.com/zrmondsc/ASSET_Development/blob/master/SupplementaryTables/EnvironmentalExclusionDatasets.xlsx).  Environmental exclusion datasets were converted to GEOTIFF format and mosaicked into a single layer. 
2. [createTechnicalInclusionAreas.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/createTechnicalInclusionAreas.ipynb): Create `Technical Inclusion Layer` based on various techno-economic criteria for renewable siting. A list of the datasets used in this analysis and an explanation of the different criteria for **solar** and **wind** can be found [here](https://github.com/zrmondsc/ASSET_Development/blob/master/SupplementaryTables/TechnoEconomicInclusionDatasets.xlsx). The technical datasets were used to create euclidean distance rasters. The euclidean distance rasters were then reclassified based on technology dependent buffer values (determined by Wu et al.) and combined using the raster calculator.  
3. [createThresholdRasters.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/createThresholdRasters.ipynb): Create `Technical Exclusion Layer` based on various techno-economic criteria for renewable siting. A list of the datasets used in this analysis and an explanation of the different criteria for **solar** and **wind** can be found [here](https://github.com/zrmondsc/ASSET_Development/blob/master/SupplementaryTables/TechnoEconomicExclusionDatasets.xlsx).
4. [maskInclusionRaster.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/maskInclusionRaster.ipynb): Create `Inclusion Area Layer` representing land area across the US that is suitable for utility scale **solar** or **wind** development. This layer is created using a raster based approach. We subtract the outputs of (1) and (3) from (2). The inclusion layer is converted to a vector for further processing and subsequent analysis. 

## 🤓 Phase 2: Area Analysis 
### Methodology and Code
We compared the results of our renewable resource assessment to a previous assessment conducted by Wu et al. (2023). In this project we sought to reproduce various elements of the 2023 study (albeit a simplified version) on a CONUS scale. Thus this area analysis was one way to understand how our results might differ from that 2023 analysis, and how those differences might compound in subsequent analyses. We used two different rectangular meshes, derived from the community earth system model (CESM2) and the 5th generation European Center for Medium-Range Weather Forecasts (ECMRWF) atmospheric reanalysis of the global climate (ERA5), as the basis for our analysis. Thus we obtained two different cell by cell comparisons of area, using the ERA5 grid cell (0.25&deg;x0.25&deg;) and the CESM2 grid cell (1.25&deg;x125&deg;) as our fundamental units. The main steps in our analysis are described below:

1. [getAreaByGrid.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/AreaAnalysis/getAreaByGridToo.ipynb):
2. [areaComparison.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/AreaAnalysis/areaComparison.ipynb):
3. [processAreaAssessment.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/AreaAnalysis/processAreaAssessment.ipynb):

## 🌐 Phase 3: Transmission Modelling 
### Methodology and Code
1.[selectByAttribute.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/TransmissionModelling/selectByAttribute.ipynb):
2.[getPointPairsTwoGeos.ipynb](https://github.com/zrmondsc/ASSET_Development/blob/master/TransmissionModelling/getPointPairsTwoGeos.ipynb):
3.[]
## Figures and Visualizations

## Requirements

  
