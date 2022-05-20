**Project Background:**  Disturbances are a part of a healthy forest ecosystem. Disturbances promote the creation of gaps in the forest canopy, which allow for new growth (Chung et al. 2022). Forest canopy gaps vary in size and shape, determined by the disturbance and ecosystem characteristics. The gaps create areas of increased resources which allows for germination and growth of new species, it can even support early successional species that require high amounts of light (Yamamoto 2000, Muscolo et al. 2014, Chung et al. 2022) Succession theory predicts that shade-intolerant species will disappear from forests and will be replaced with shade-tolerant species (Yamamoto 2000). Since disturbances create canopy gaps they are directly associated with regeneration and succession(Yamamoto 2000, Chung et al. 2022). These areas often end up being targeted by restoration efforts due to the opportunity for regeneration.
  In Baltimore, MD the forest is rather urban ranging from small patches to large semi-natural forests. Due to the proximity of these forests, they are plenty of anthropogenic disturbances that can cause forest gaps.  Do the proximity to densely populated areas correlated with the size of forest canopy gaps? In this identification, the R package GetForestGapsR will be utilized through the analysis of the 2015 Maryland LiDAR (Silva et al. 2019).

### 1. Preparing LiDAR Data and GetForestGapsR

To prepare the LiDAR point cloud data a canopy height model was created by creating rasters of first return and ground returns. These rasters were then used to calculate the canopy height model. With the canopy height model rasters the GetForestGapsR toolbox could be applied, as displayed in the code below.


<img src="/final_project/get_forest_gap.png?raw=true"/>


This code was repeated for multiple canopy height models that make up Gwynns Falls and Leakin Park in western Baltimore, MD. The R package also allows for the calculation of statistics and the creation of shapefiles. The map provided below displays the forest canopy gaps (red polygons) present in the two parks of interest. 


<img src="/final_project/gaps_layout.png?raw=true"/>

### 2. Calculating Population Density and Summarizing Gaps 

With the forest canopy gaps identified, the population density can be calculated. As seen in the code below, using tidy census allowed for the total population to be pulled for Baltimore tracts. The area and the population density (pop/sq.mi.) were then both calculated and then creation of centroids for the tracks and Buffer for 0.3 and 0.5 miles. 


<img src="/final_project/pop_data.png?raw=true"/>

Using the tool Summarize Within from GIS, the sum of area and count of gaps within each buffer was calculated supplying the two maps below. The summarized areas were then plotted to produce the below graphs that show there is not a direct correlation with increasing population density and the total area of gaps. 


<img src="/final_project/twomaps.png?raw=true"/>

<img src="/final_project/two_graphs.png?raw=true"/>

### 3. Discussion 

This methodology and results would benefit from a comparison site that has less gaps or smaller population densities, to compare as whole sites not just tracts within the same study reach. There also needs to be consideration of the Modifiable Aerial Unit Problem (MAUP) as tracts very in size throughout the study reach as well as Baltimore, MD in general. To adjust for MAUP, a hexagonal grid could be added making the areas the same size but would be using an approximation of population density.  

### 4. Data Sources and References 

Data Sources:
Maryland LiDAR 2015: imap.maryland.gov
Census Total Populations: U.S. Census Bureau: American Community Survey 2020
References:
Chung, C.-H., J. Wang, S.-L. Deng, and C. Huang. 2022. Analysis of Canopy Gaps of Coastal Broadleaf Forest Plantations in Northeast Taiwan Using UAV Lidar and the Weibull Distribution. Remote Sensing 14:667.
Muscolo, A., S. Bagnato, M. Sidari, and R. Mercurio. 2014. A review of the roles of forest canopy gaps. Journal of Forestry Research 25:725–736.
Silva, C. A., R. Valbuena, E. R. Pinagé, M. Mohan, D. R. A. de Almeida, E. North Broadbent, W. S. W. M. Jaafar, D. de Almeida Papa, A. Cardil, and C. Klauberg. 2019. ForestGapR: An r Package for forest gap analysis from canopy height models. Methods in Ecology and Evolution 10:1347–1356.
Yamamoto, S.-I. 2000. Forest Gap Dynamics and Tree Regeneration. Journal of Forest Research 5:223–229.



