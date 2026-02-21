# GEE Concepts  

For the first week, we will cover the following three topics:
 
* A class project proposal  
* A quick quiz  
* How EE works
* EE objects, methods and functional programming
* Introduction to the Earth Engine JavaScript API 


## A class project proposal 
* Start a research topic
* Literature review 
* One papers on GEE ([paper1](ref/GEE_Gorelick_RSE2017_1-s2.0-S0034425717302900-main.pdf) and [paper2](ref/GEE_RSE2020_1-s2.0-S0034425720303722-main.pdf) )

## A quick quiz on last week's material
 Go to code.earthengine.google.com, start GEE code editor, and perform the following tasks: 
* Use GEE to create an object of a city with city name, latitude, longitude, and population density, and print out the properties of an object
* Use GEE to write a function to calculate NDVI using band4 and band3 as inputs 
* Run your code, share your output in class
* You should not repeat the examples in the lab section


## [How EE works](https://developers.google.com/earth-engine/guides/concepts_overview)
* Client vs server
* Scale
* Projections - Reproject should be avoided
* Resampling and reducing resolution


## EE objects, methods and functional programming    
Now that you're comfortable with JavaScript, learn how to put JavaScript objects and primitives into Earth Engine containers for sending to the server and processing at Google. Here is [reference](https://developers.google.com/earth-engine/tutorials/tutorial_js_02) for this section. 


### [EE objects and methods](https://developers.google.com/earth-engine/tutorials/tutorial_js_02)
* Strings
* Numbers
* Methods on Earth Engine objects
* Lists
* Casting
* Dictionaries
* Dates
* Digression: passing parameters by name
* 

### [EE functional programming](https://developers.google.com/earth-engine/tutorials/tutorial_js_03)
* Avoid loops
* Avoid conditions

## [Analysize data](https://developers.google.com/earth-engine/tutorials/tutorial_api_01) 
* [ee.Image](https://developers.google.com/earth-engine/guides/image_overview) - raster data types. Images are composed of bands and a dictionary of properties.  
* [ee.ImageCollection](https://developers.google.com/earth-engine/guides/ic_creating) - handles a stack of images (e.g. an image time series) 

## Lab 2

### GEE:
1. Use the GEE imagecollection function to read  Landsat data (surface reflectance) for any period
2. Get clearest images from your landsat image collection
3. Write a function  to calculate the normalized difference of vegetation index (NDVI = (NIR band- red band)/(NIR_band + Red_band))
4. Use the map function to calculate the NDVI image
5. Display the NDVI image in the any region
   
### Research
1. Read at least one research paper on your topic, ideally from the Remote Sensing of Environment journal, and be ready to share with the class next week on the research problem, research method, results, and conclusion. 




