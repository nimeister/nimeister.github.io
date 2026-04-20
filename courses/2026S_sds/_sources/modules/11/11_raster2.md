## 11 - Raster Data Analysis II 

[Jenning creek fire](https://www.youtube.com/watch?v=aJaFHSgKLXI)


## Table of Contents

1. [Multispectral Data- Sentinel-2](#1)
2. [Geospatial tools](#2)
3. [Processing raster data](#3)
4. [Geospatial tool Installation](#4)   
5. [Exercises](#5)

## 1. Multispectral Data 

### What is multispectral satellite data 

#### [Landsat 8](https://www.earthdatascience.org/courses/use-data-open-source-python/multispectral-remote-sensing/landsat-in-Python/)

### Access Satellite Data
#### [Earth Explorer](https://earthexplorer.usgs.gov/) and here is a [video](https://www.youtube.com/watch?v=qUhcKp5tLXY) to demonstrate how to download a landsat 8 or 9 imagery.
#### On Cloud
- [amazon cloud](https://www.usgs.gov/landsat-missions/landsat-commercial-cloud-data-access)
- [google cloud](https://developers.google.com/earth-engine/datasets/catalog/landsat)

## 2. Geospatial tools 
### Xarray
[Xarray](http://xarray.pydata.org/en/stable/), N-D labeled arrays and datasets in Python, is an open source project and Python package that makes working with labelled multi-dimensional arrays simple, efficient, and fun! Xarray is inspired by and borrows heavily from pandas, the popular data analysis package focused on labelled tabular data. It is particularly tailored to working with netCDF files, which were the source of xarray’s data model, and integrates tightly with dask for parallel computing.

### Rioxarray 
[Rioxarray](https://corteva.github.io/rioxarray/stable/) combines xarray and rasterio, similar to how geopandas combines functionality from pandas and fiona. This module is an extension for xarray to provide rasterio capabilities to xarray datasets/dataarrays. Some functions include: 
- Resampling
- Convert dataset to raster (GeoTiff)
- Clip
- Clip Box
- Pad Box
- Reading COGs in Parallel
- Reproject
- Reproject Match (For Raster Calculations/Stacking)
- Merge
- Interpolate Missing Data
- Transform Bounds
- Cloud Optimized GeoTiff (COG)
- Reading and Writing with Dask
- Zonal Statistics


### Differences between rasterio and rioxarray
Feature | Rasterio | Rioxarray |
|---------|----------|-----------|
| **Abstraction Level** | Low-level (GDAL wrapper) | High-level (built on rasterio + xarray) |
| **Data Structure** | NumPy arrays | xarray DataArrays/Datasets |
| **Metadata Handling** | Separate dictionaries | Integrated with data object |
| **Dependencies** | GDAL, NumPy | Rasterio, xarray, NumPy |
| **Coordinate Labels** | No (index-based only) | Yes (named dimensions, coordinates) |
| **Multi-dimensional Data** | Manual management | Native support (time, bands, etc.) |
| **Lazy Loading** | No (loads to memory) | Yes (via Dask integration) |
| **File I/O Control** | Precise, granular control | Simplified, abstracted |
| **CRS Management** | Manual tracking | Automatic (stored with data) |
| **Parallel Processing** | Manual implementation | Built-in (Dask support) |
| **Learning Curve** | Steeper (closer to GDAL) | Gentler (if familiar with pandas/xarray) |
| **Memory Efficiency** | More control, but manual | Automatic chunking available |
| **Use Case** | Low-level operations, format conversion | Analysis workflows, multi-dimensional data|
| **Syntax Style** | Context managers, explicit reads | Method chaining, pandas-like |
| **NetCDF Integration** | Limited | Excellent (native xarray feature) |
| **Performance** | Generally faster for simple operations | Overhead but better for complex workflows |


### Earthy

[EarthPy](https://pypi.org/project/earthpy/) builds upon the functionality developed for raster data (rasterio) and vector data (geopandas) in Python and simplifies the code needed for many image processing. Some functions include:
- Stack and crop raster bands from data such as Landsat into an easy to use numpy array
- Work with masks to set bad pixels such a those covered by clouds and cloud-shadows to NA (mask_pixels())
- Plot rgb (color), color infrared and other 3 band combination images (plot_rgb())
- Plot bands of a raster quickly using plot_bands()
- Plot histograms for a set of raster files.
- Create discrete (categorical) legends
- Calculate vegetation indices such as Normalized Difference Vegetation Index (normalized_diff())
- Create hillshade from a DEM


## Geospatial tool Installation <a id=3></a>
  
Note: If you are using miniforge, use the following commands to install: 
- `conda install rioxarray`
- `conda install earthpy`
- `conda install dask`
  
If you are using Anaconda/miniconda, then you need to use the following commands to install:
- `conda install conda-forge::rioxarray`
- `conda install conda-forge::earthpy'
- `conda install dask'


## Exercises
1. [Notebook #1](01_ortho_rioxarray.ipynb)
2. [Notebook #2](02_jenningscreekfire.ipynb)

## Homework
Assessment of the Impact of the Jones Road Wildfire in NJ in Spring 2025
- Read the [NYC article](https://www.nytimes.com/2025/04/22/nyregion/wildfire-new-jersey-ocean-county.html)
- Find out the [Fire location](https://6abc.com/post/nj-wildfire-maps-show-location-ocean-county-new-jersey-blaze-current-road-closures/16230917/)
- Download the boundary (shape file or geojson files) of Barnegat Township in Ocean County, New Jersey or the whole Ocean County. [This](https://planning.co.ocean.nj.us/frmDMGeographic) maybe  a site you can download.
- Download the Landsat 8 or 9 imageries one in summer 2025 and one in 2024 from this link: [Earth Explorer](https://earthexplorer.usgs.gov/), unzip them into a directory 
- Use rioxarray  to open and read these two landsat imates, climp them for the Ocean County 
- Calculate and compare NDVI images for 2024 and 2025 summer
- Calculate and display the NDVI difference for these two years 

## References: 
- https://www.earthdatascience.org/courses/use-data-open-source-python/multispectral-remote-sensing/
- https://carpentries-incubator.github.io/geospatial-python/
