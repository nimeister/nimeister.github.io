# 06 - Data Visualization  

## Overview
We went over some basic concepts on pandas and numpy last week. For this week, we will learn to analyize real data using python visualization tools. Data visualization is the graphical representation of data through graphs, charts, maps, etc.  It allows data to tell its own story without imposing any assumptions or models. In other words, data visualization allows the data to speak for itself! 

Python offers multiple great [graphing libraries](https://towardsdatascience.com/top-6-python-libraries-for-visualization-which-one-to-use-fe43381cd658) with many different features. Matplotlib is the most basic one and others build on it. Matplotlib is the most used Python package for data visualization. It provides both a quick way to visualize data from Python and publication-quality figures in many formats. Many other packages like pandas plotting and seaborn, were built on Matplotlib.In this module, we will focus on understanding the basic matplotlib, then learn pandas simple plot functions and introduce some basic plotting and statistical analysis functions in seaborn. 


## Matplotlib Package

### References: 
1. [Matplotlib](https://matplotlib.org/stable/).
2. [Pandas.pivot_table at SciPy 2021](https://github.com/chendaniely/2021-07-13-scipy-pandas)

## Pandas Data Visualization
Pandas, Python’s popular data analysis library, also provides several different options for visualizing your data with .plot().
We will learn to create basic plots using pandas plot() functions to start our visualization journey. 
Meanwhile, we will also continue to learn Pandas data manipulation functions with pandas.plot() in today's exercises. 

## hvPlot
[hvplot()](https://hvplot.holoviz.org/en/docs/latest/tutorials/getting_started.html) is a powerful and interactive Pandas-like .plot() API. By replacing .plot() with .hvplot(), you get an interactive figure. 
You need to install hvplot first under your miniforge prompt using 

`conda install hvplot` 
or 

`pip install hvplot`

Then `import hvplot.pandas`, then you can call .hvplot() on the DataFrame as you would call Pandas’ .plot().

### Exercises    
1. [Matplotlib](6.1.ipynb)
2. [Pandas plotting ](6.2.ipynb)
3. [Air quality data analysis](AQI_v1.ipynb)
4. [Air quality data analysis](AQI_v2.ipynb)
5. [Week 6 exercises](wk6.ipynb)
   

### References: 

1. [Introduction to data visualization in Python](https://towardsdatascience.com/introduction-to-data-visualization-in-python-89a54c97fbed)
2. [Pandas data visualization](https://pandas.pydata.org/pandas-docs/stable/user_guide/visualization.html)
3. [Data Visualization](https://www.tableau.com/learn/articles/data-visualization)



