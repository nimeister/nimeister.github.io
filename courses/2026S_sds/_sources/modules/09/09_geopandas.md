## 09 - Geopandas

This week, we are going to cover several fundamental geospatial data concepts, including coordinate systems, projections/transformations, vector geometries (points, lines, polygons) and basic geometry operations (intersect, buffer, etc). We will also begin using the [GeoPandas package](https://geopandas.readthedocs.io/en/latest/).

GeoPandas, as the name suggests, extends the popular data science library pandas by adding support for geospatial data.
“GeoPandas is an open source project to make working with geospatial data in Python easier. GeoPandas extends the datatypes used by pandas to allow spatial operations on geometric types. Geometric operations are performed by shapely. Geopandas further depends on fiona for file access and descartes and matplotlib for plotting.”

### Data Structure - Vector and Raster

The two primary types of geospatial data are raster and vector data. Raster data is stored as a grid of values which are rendered on a map as pixels. Each pixel value represents an area on the Earth’s surface. Vector data structures represent specific features on the Earth’s surface, and assign attributes to those features. 

#### [Raster Data](https://datacarpentry.github.io/organization-geospatial/01-intro-raster-data.html) 
Raster data is any pixelated (or gridded) data where each pixel is associated with a specific geographical location. The value of a pixel can be continuous (e.g. elevation) or categorical (e.g. land use). A geospatial raster is only different from a digital photo in that it is accompanied by spatial information that connects the data to a particular location. This includes the raster’s extent and cell size, the number of rows and columns, and its coordinate reference system (or CRS). We will discuss more on raster data next two weeks. 

#### [Vector Data](https://datacarpentry.github.io/organization-geospatial/02-intro-vector-data.html)
Vector data structures represent specific features on the Earth’s surface and assign attributes to those features. Vectors are composed of discrete geometric locations (x, y values) known as vertices that define the shape of the spatial object. The organization of the vertices determines the type of vector that we are working with: point, line or polygon.
- Points: Each point is defined by a single x, y coordinate. There can be many points in a vector point file. Examples of point data include: sampling locations, the location of individual trees, or the location of survey plots.
- Lines: Lines are composed of many (at least 2) points that are connected. For instance, a road or a stream may be represented by a line. This line is composed of a series of segments, each “bend” in the road or stream represents a vertex that has defined x, y location.
- Polygons: A polygon consists of 3 or more vertices that are connected and closed. The outlines of survey plot boundaries, lakes, oceans, and states or countries are often represented by polygons.

A line shapefile that contains the locations of streams, might contain the name of each stream. Because the structure of points, lines, and polygons are different, each individual shapefile can only contain one vector type (all points, all lines or all polygons). You will not find a mixture of point, line and polygon objects in a single shapefile.

### [Coordinate reference system (CRS)](https://carpentries-incubator.github.io/geospatial-python/03-crs.html)
The CRS associated with a dataset tells your mapping software where the raster is located in geographic space. It also tells the mapping software what method should be used to flatten or project the raster in geographic space.

#### Three components of CRS information
- **Datum**: A model of the shape of the earth. Common global datums are WGS84 and NAD83
- **Projection**: A mathematical transformation of the angular measurements on a round earth to a flat surface.
- **Additional parameters**: One common additional parameter is a definition of the center of the map. The number of required additional parameters varies by each specific projection.

#### Describing Coordinate Reference Systems
Several common systems are in use for storing and transmitting CRS information, as well as translating among different CRSs. These systems generally comply with ISO 19111. Common systems for describing CRSs include EPSG, OGC WKT, and PROJ strings.

- **EPSG** 
The EPSG system is a database of CRS information maintained by the International Association of Oil and Gas Producers. The dataset contains both CRS definitions and information on how to safely convert data from one CRS to another. Using EPSG is eas,y as every CRS has an integer identifier, e.g. WGS84 is EPSG:4326. The downside is that you can only use the CRSs defined by EPSG and cannotcustomizee them (some datasets do not have EPSG codes). epsg.io is an excellent website for finding suitable projections by location or for finding information about a particular EPSG code.

- **Well-known Text (WKT)** is the
The Open Geospatial Consortium WKT standard has several important geospatial apps and software libraries. WKT is a nested list of geodetic parameters. The structure of the information is defined on their website. WKT is valuable in that the CRS information is more transparent than in EPSG, but it is a more complex CRS system, but it can be more difficult to read.

- **PROJ** is an open-source library for storing, representing and transforming CRS information. There are some issues with reprojecting. It is best to only use PROJ strings as a format for viewing CRS information, not for reprojecting data.

### Essential Geospatial Python libraries to Process Vectors
#### [Shapely](https://shapely.readthedocs.io/en/stable/manual.html) 
With shapely, you can create shapely geometry objects (e.g. Point, Polygon, Multipolygon)
and manipulate them, e.g. buffer, calculate the area or an intersection etc. Shapely itself does not provide options to read/write vector file formats (e.g. shapefiles or geojson) or handle projection conversions. 

#### [Fiona](https://fiona.readthedocs.io/en/latest/manual.html) 
Fiona reads/writes vector file formats (e.g. shapefiles or geojson) or handles projection conversions. 

#### [Geopandas](https://geopandas.org/en/stable/docs/user_guide.html) 
Geopandas combines the geometry objects of shapely, the read/write/ projection functions of fiona and the powerful dataframe interface of the pandas library in one awesome package. In the spreadsheet-like dataframe, the last column ‘geometry’ stores the shapely geometry objects, all shapely functions can be applied. The pandas mechanics offer super easy ways to manipulate, plot and analyze the data, e.g. dataframe groupby operations etc.

#### GeoPandas and Arcpy 
GeoPandas does not have all the functions that arcpy provides — but it covers many core vector-analysis capabilities, and in combination with other open-source libraries, you can do nearly everything arcpy does.

| Category | **ArcPy (Esri)** | **GeoPandas + Open-Source Stack** | Comments / Notes |
|-----------|------------------|-----------------------------------|------------------|
| **License** | Proprietary (requires ArcGIS Pro license) | Free & open-source (BSD, MIT, GPL) | ArcPy tied to Esri licensing system |
| **Core focus** | Comprehensive GIS platform (vector, raster, 3D, map automation) | Primarily vector + 2D analysis, extended by other libs | GeoPandas ecosystem modular |
| **Main data model** | Esri Feature Class / Geodatabase | GeoDataFrame (based on pandas) | GeoDataFrame more Pythonic |
| **Data formats supported** | Esri GDB, Shapefile, Feature Service | Shapefile, GeoJSON, GeoPackage, PostGIS, Parquet, etc. | GeoPandas + Fiona highly flexible |
| **Vector operations** | Buffer, Clip, Dissolve, Intersect, Union, Spatial Join, Select | Buffer, Overlay, Spatial Join, Dissolve, Query | Mostly equivalent via `geopandas` + `shapely` |
| **Projection / CRS** | Managed via `arcpy.management.Project` | `gdf.to_crs()` using `pyproj` | Both support full EPSG/PROJ transforms |
| **Attribute management** | Field calculator, cursors | Pandas-style DataFrame ops (`.loc`, `.apply`) | Open-source syntax often simpler |
| **Raster processing** | Strong via `arcpy.sa` (Spatial Analyst) | `rasterio`, `rioxarray`, `xarray`, `rasterstats` | ArcPy has tighter GUI integration |
| **3D / LiDAR** | `arcpy.ddd`, LAS dataset tools | `PDAL`, `laspy`, `pyntcloud` | PDAL very powerful, but coding required |
| **Network / routing** | `arcpy.na` (Network Analyst) | `osmnx`, `networkx`, `openrouteservice` | Open alternatives free but less GUI-based |
| **Geostatistics** | `arcpy.ga` (kriging, IDW, semivariograms) | `pykrige`, `gstools`, `scikit-gstat` | ArcPy has GUI tools; open tools require code |
| **Topology validation** | Built-in topology rules | Limited (geometry validity checks only) | Shapely supports `.is_valid`, `.buffer(0)` fixes |
| **Cartography / layout automation** | `arcpy.mp` for ArcGIS Pro map documents | `matplotlib`, `cartopy`, `contextily`, `folium` | ArcPy can control ArcGIS layouts directly |
| **Database / server integration** | Enterprise geodatabases, ArcGIS Server | PostGIS (via GeoAlchemy2), SpatiaLite, WFS/WMS | Open stack supports many open standards |
| **Performance** | Optimized C++/C behind ArcGIS tools | Python-level, vectorized via NumPy/Shapely | GeoPandas slower on huge datasets; use Dask/GeoParquet for scale |
| **Environment** | Controlled via ArcGIS Pro Conda (`arcgispro-py3`) | Standard conda/pip environments | Easier package management in open stack |
| **Platform compatibility** | Windows only | Cross-platform (Windows, macOS, Linux) | ArcPy tied to ArcGIS Pro on Windows |
| **Community & support** | Esri Tech Support, Pro Docs | Active OSS community, Stack Overflow, GitHub | Both well-documented but different ecosystems |
| **Automation & scripting** | Python scripting inside ArcGIS Pro | Pure Python scripts, Jupyter Notebooks | Open stack ideal for data-science workflows |
| **Cost** | $$$ (ArcGIS Pro license) | $0 | Open-source advantage for research and teaching |
| **Ease of learning** | GUI + Python scripting | Code-centric (pandas-like) | GeoPandas more intuitive for data scientists |
| **Typical use cases** | Enterprise GIS, cartographic production, regulatory datasets | Research, automation, data science, reproducible analysis | Many users combine both |


#### Geospatial packages Installation 
You can install all required packages for geospatial analysis using minforge:
- conda install geopandas
- conda install geodatasets

### Exercises    
1. [Geopandas Notebook](01_IntroGeopandas.ipynb)

### References: 

1. https://geopandas.org
2. https://geohackweek.github.io/vector/
3. https://datacarpentry.github.io/organization-geospatial/
4. https://carpentries-incubator.github.io/geospatial-python/
5. https://www.earthdatascience.org/courses/use-data-open-source-python/intro-vector-data-python/



