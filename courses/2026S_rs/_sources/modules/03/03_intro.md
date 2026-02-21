# GEE Objects and Methods  

For the first week, we will cover the following three topics:
 
* Research project ideas
* More Earth Engine Objects and Methods 
* Earth Engine  API 

## Share your research project ideas 
* HWK - Find a paper related to your research topic using GEE, be ready to share in class

## [Earth Engine Objects and Methods](https://developers.google.com/earth-engine/guides/objects_methods_overview)

* [ee.Image](https://developers.google.com/earth-engine/guides/image_overview) - raster data types. Images are composed of bands and a dictionary of properties.  
* [ee.ImageCollection](https://developers.google.com/earth-engine/guides/ic_creating) - handles a stack of images (e.g. an image time series) 
* [ee.Geometry](https://developers.google.com/earth-engine/guides/geometries) - handles vector data
* 
## Some tips of using Code Editor
* Hit back slash keyboard to see all the shortcut
* Undo: Ctrl + Z
* Redo: Ctrl + Shift + Z

## Lab3 
* Write your own GEE code to read a Sentinel-2 scene for a location you select from the map as demonstrated in class, filter out by your selected dates and cloud cover less than 5%.
* Mask out the cloud using the example from this [link](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED)
* Display a false color composite image of the median of all the image collections 
* Draw a polygon on the map for your study area, and clip the image for your area. If you have a shape file for your study area, you can upload it to your assets and then clip.
* Display a false color composite image of the median of all the image collections for your clipped area  
* Calculate and display NDVI and NDWI images ( NDVI=(NIR-RED)/(NIR+RED); NDWI = (Green- shortwave band)/(Green+ shortwave band) of for your clipped area
* You also have the choice to explore the satellite data you want to use for your research. If your satellite does not provide NDVI and NDWI, it is also fine to display other parameters.
* Review a research paper and share it in class