**Project description:** Chapters 1-4 of Cutts and Graser "Learn QGIS" walks users through the basics uses and application of QGIS. Within these chapster the reader walks through tutorials of the decribed skills. Following the tutorials, I enhances three of the maps to continue developing new QGIS skills.

### 1. Provinces & Territories of Canada

The map was enhanced through additional imformation. The polygon shapefile was obtained by USGS and the population data and flags were obtained through Wikipedia. 

```javascript
if (isAwesome){
  return true
}
```

### 2. Alaska Global Landcover Classification

To enhance the landcover map I started by using Extract by Mask on the Hillshade. 
This gave the look of nice clean edges for the Alaska polygon. With both a hillshade and the 
landcover raster the landcover transcpareency was increased to allot for the hillshade. 

```javascript
if (isAwesome){
  return true
}
```

### 3. Airports within Alaskan Regions

Finally this map displays Alaskan Airports differentiated by use. Using the count tool, QGIS created a new field in the Regions indicating the number of airports within their region.

