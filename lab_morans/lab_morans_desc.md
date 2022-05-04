**Project description:** Chapters 1-4 of Cutts and Graser "Learn QGIS" walks users through the basics uses and application of QGIS. Within these chapster the reader walks through tutorials of the decribed skills. Following the tutorials, I enhances three of the maps to continue developing new QGIS skills.

### 1. Moran's I Calculation for the Percent of Baltimore City Tracts that Received SNAP Benefits

The map provide people show the layout of percent of people within each tract who received SNAP benefits. The central portions of the city display to have higher percentages of people receiving SNAP. With a Moran’s I of 0.47 there is a less than 1 % chance that this clustered pattern is a result of random chance.


<img src="/lab_morans/receive_snap?raw=true"/>

### 2. Moran's I Calculation for Percent of the Non-Hispanic Black Population

To enhance the landcover map I started by using Extract by Mask on the Hillshade. 
This gave the look of nice clean edges for the Alaska polygon. With both a hillshade and the 
landcover raster the landcover transcpareency was increased to allot for the hillshade. 

<img src="/lab1/Alaska_map.png?raw=true"/>

### 3. Airports within Alaskan Regions

Finally this map displays Alaskan Airports differentiated by use. Using the count tool, QGIS created a new field in the Regions indicating the number of airports within their region.

<img src="/lab1/alaska_airport_map.png?raw=true"/>
