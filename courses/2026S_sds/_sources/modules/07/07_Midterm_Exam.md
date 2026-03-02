# 07 - Midterm Exam

## Instruction: 
The midterm exam is like a mini-project. It is an open-book exam. 
The requirement is you will need to come up a research question, propose a methodology to answer 
your research question and implement it in Python. Your project should use **four out of six** Python features we covered in class: 

- Use Python, pandas, or numpy's indexing and slicing features to extract your data;
- Use numpy the `where` function
- Use the `groupby` features to sort your data  
- Use matplotlib visualization tools to display your results
- Use functions to make your code concise; get a bonus if using `class` feature

All the information should be included in a Jupyter notebook: 

Your Jupyter notebook should be mixed Markdown Cells and Code Cells:
- Markdown Cell: Title of your project
- Markdown Cell: The research question you propose to answer
- Markdown Cell: The proposed method - itemizing each Python feature you propose to use. 
- Code Cell (as many as you need) - each code cell should include a comment line first on what you are trying to do below, followed by Python code.
- Codel Cell (as many as you need) - visualizing your results
- Markdown cell: summarizing your final results. 

Below, I provide some datasets and associated example research questions:  

## 1. NYC street tree data analysis 
### NYC tree data:
Tree census data collected in 1995, 2005, and 2015 are freely available from [NYC Opendata portal](data.https://opendata.cityofnewyork.us/). More information on the tree count project can be found [here](https://www.nycgovparks.org/trees/treescount)
More information on the data format can be found in the following links: 
- [2015 tree census data](https://data.cityofnewyork.us/Environment/2015-Street-Tree-Census-Tree-Data/uvpi-gqnh)
- [2005 tree census data](https://data.cityofnewyork.us/Environment/2005-Street-Tree-Census/29bw-z7pj)
- [1995 tree census data](https://data.cityofnewyork.us/Environment/1995-Street-Tree-Census/kyad-zm4j)

### Research questions
- How much carbon is stored in NYC street trees? 
- How fast do NYC street trees grow? (dbh or height histogram) ?
- What is the carbon sequestration rate of NYC street trees (carbon stock differences)?


## 2. Air Quality Data Analysis
### [EPA Air Quality Data](https://aqs.epa.gov/aqsweb/airdata/download_files.html#Meta). 
- [Differences among AQI, PM25, O3](https://forum.airnowtech.org/t/the-aqi-equation/169)
### [PurpleAir quality data](https://www2.purpleair.com/)


### Example Research questions 
- Does the air quality (different air quality parameters) have any temporal patterns? Why?
- Impact of COVID shutdown on air quality:
    - Was the air quality improved after the COVID-19 shutdown for New York City? 
    - Where in the US has the maximum impact on air quality due to the COVID shutdown? 
    - Does the air quality improvement have any spatial variations? Does it have a bigger impact on urban areas than suburban areas?      
- Impact of fires on air quality
    - What is the impact of fires on air quality? 
    - Any spatial and temporal variations? 
    - Do fires only affect local air quality or do they affect the air quality at a large scale?
    - 
## 3. NYC energy use and Greenhouse Gas (GHG) emissions
### [Data Portal](https://data.cityofnewyork.us/Environment/NYC-Greenhouse-Gas-Emissions-Inventory/wq7q-htne/about_data)
- 
### Example Research questions 
- What are the spatial and temporal patterns of the energy use and GHG emissions? 

## 4. NYC transportation data 
### [The New York State Department of Transportation (NYSDOT) Drakewell Traffic Data Porta](https://nysdottrafficdata.drakewell.com/)

### Example Research questions 
- What are the spatial and temporal patterns of NYC traffic volume counts?
- How is the traffic volume count related to GHG emissions in areas and buildings you pick  
- How does the [NYC Congestion Pricing Program](https://congestionreliefzone.mta.info/about) affect the traffic count and the GHG emissions 


## 5. NYC water quality data analysis
### Data Portal

1. Water Quality Data, NYS DEC    :
- https://dec.ny.gov/environmental-protection/water/water-quality/monitoring/water-quality-da  
- Data archive: https://experience.arcgis.com/experience/301748017d7d40649bc5082fc1c53blooms

2. Harbor Water Quality, NYCDEP
- https://data.cityofnewyork.us/Environment/Harbor-Water-Quality/5uug-f49n/about_data

3. National Water Quality data 
- https://www.waterqualitydata.us/
- https://www.epa.gov/waterdata/water-quality-data
  
### Example Research questions 
- What are the spatial and temporal patterns of harmful algae, CDOM, and nutrient levels in NYC waterbodies? 

## Use your own data and formulate your own research questions 
