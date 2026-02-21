# 01 - Data Science & Jupyter Notebook

Welcome to the journey to Spatial Data Science/GeoComputation 1. For the first week, we will cover the following three topics:
 
* Introduction to data science and spatial data science
* Required software setup
* Navigate a [Jupyter Lab](https://jupyter.org/) environment

# Table of Contents
- Data Science and Spatial Data Science
- Conda and Jupyter Setup Instructions
- Navigate the Jupyterlab Environment
- Install Packages
  
## Data Science and Spatial Data Science

### Data Science
In our modern world, we confront abundant datasets,
which are valuable for advancing our scientific goals. But we need the computational skills to make full use of vast amount datasets.

Data Science is a child of statistics and computer science.

![Data Science](img/DS.png)

A few popular jokes: 

"A data scientist is a statistician who lives in San Francisco." 

“A data scientist is a statistician who is useful.”

[What Do Data Scientists Do?](https://www.coursera.org/articles/what-is-a-data-scientist)

What are the most in-demand skills for data scientists in the [job market](https://365datascience.com/career-advice/career-guides/data-scientist-job-outlook-2025/#h_7765086379621741854115110)?

If you want to know what Python skills are for a data scientist, check out [Python Data Science Handbook](https://github.com/jakevdp/PythonDataScienceHandbook/tree/master/notebooks)


### GeoSpatial Data Science

In the environmental science field, more Earth observation data are being collected each day. A few examples: 
- Many satellites are in space and constantly collecting data about our planet, Earth, each day. You can find more on [NASA Earth science missions](https://science.nasa.gov/earth-science). 
- Many large network field data are being collected, two examples: 
[The National Ecological Observatory Network, or NEON](https://www.neonscience.org/) is collecting ecological data from sites across the continental scale. 
- Ground sampling data, for example, [NYC open data portal](https://opendata.cityofnewyork.us/)
  
[Spatial Data Analytics: The What, Why, and How?](https://www.velotio.com/engineering-blog/spatial-data-analytics-the-what-why-and-how)

Spatial data science is an emerging field that combines data science techniques with geospatial analysis to understand and solve problems related to the location and spatial relationships of phenomena on Earth. It involves using tools and methods to analyze, visualize, and interpret spatial data, revealing patterns, trends, and insights that can inform decision-making in various sectors. 

Spatial data science merges several areas, including:

- Geospatial Analysis: The study and interpretation of geographic data through spatial algorithms.
- Machine Learning: The use of statistical models and machine learning algorithms to make predictions or discover patterns in geospatial data.
- Data Visualization: Creating maps, charts, and other visualizations that represent the spatial distribution of data.
- Spatial Statistics: Applying statistical techniques to understand spatial patterns and relationships.

For this class, we will learn basic Python skills to obtain, analyze, and visualize those large environmental datasets. 

It will be beneficial and helpful if you have or are taking a remote sensing course. Otherwise,  you can learn some background on remote sensing by watching some [online turorials](https://www.earthdata.nasa.gov/data/projects/arset).

What is the average salary for a [geospatial data scientist?](https://www.ziprecruiter.com/Salaries/Geospatial-Data-Scientist-Salary)?

## Conda and Jupyter Setup Instructions

### Basic Terminology

#### Python 
- A software is distributed as a series of *libraries* that are called within your code to perform certain tasks. 
- There are many different collections, or *distributions* of Python software. Generally you install a specific distribution of Python and then add additional libraries as you need them. 
- There are also several different *versions* of Python. Support for Python 2 ended in 2020, so you should use Python>=3

#### Jupyter Notebook
- Jupiter Notebook is an open-source web application that allows you to create and share documents that contain live code, equations, visualizations and narrative text. 
- Contain live code, equations, visualizations and explanatory text such as figures, links and equations
- Can be executed perform the data analysis in real time  
- “Jupyter" is a loose acronym meaning Julia, Python, and R. also supports many other languages. 
- The Jupyter Notebook App allows you to edit and run your notebooks via a web browser. 

- The application can be executed on a PC without Internet access, or it can be installed on a remote server, where you can access it through the Internet.

#### Jupyter Lab
- JupyterLab is the latest web-based interactive development environment for notebooks, code, and data. Its flexible 
interface allows users to configure and arrange workflows in data science, scientific computing, computational journalism, and machine learning. 
It provides flexible building blocks for interactive, exploratory computing. 
- We will use Jupyter lab for this class.

#### Anaconda (not recommended)
- [Anaconda](https://www.anaconda.com/distribution/) is a data science platform that comes with a lot of packages/libraries.
Anaconda is a distribution of the Python and R programming languages for scientific computing (data science, machine learning applications, 
large-scale data processing, predictive analytics, etc.), that aims to simplify package management and deployment. 
Anaconda offers the easiest way to perform Python/R data science and machine learning on a single machine.

- You can install Python and Jupyter notebook and conda by installing Anaconda. It particularly works better for beginners.

- The list of packages included can be found [*here*](https://www.anaconda.com/).

#### Miniconda (not recommended)
- [Miniconda](https://docs.conda.io/en/latest/miniconda.html) is a free minimal installer for conda. It is a small, bootstrap version of Anaconda that includes only conda, Python, the packages they depend on, and a small number of other useful 
packages, including pip, zlib and a few others. If you don't want Anaconda to take a lot of space, 
use minconda.  

#### Miniforge (Recommended)
- [Miniforge](https://github.com/conda-forge/miniforge) is a minimal installer for Conda that uses the conda-forge channel by default instead of Anaconda’s defaults.
This gives you fresher packages and broader coverage, especially for scientific and geospatial software.
- Like Miniconda, it only installs Conda + Python + a few basics.
- In this class, we recommend you install miniforge 


#### Conda
- Package versions in Anaconda are managed by the package management system conda
- [**Conda**](http://conda.pydata.org/docs/) is an **open source `package` and `environment` management system** 
- If you want to learn more in-depth on Conda, check this [link](https://github.com/UW-GDA/gda_course_2021/blob/master/resources/conda.md)
 or this [link](https://carpentries-incubator.github.io/introduction-to-conda-for-data-scientists/02-working-with-environments/index.html).

### Setup your environment

#### Install Conda
Download and install the Python 3 version of conda.

- (Not Recommended) Install Anaconda, follow the instructions [here](https://www.anaconda.com/download/) or 
watch this [Youtube](http://swcarpentry.github.io/python-novice-gapminder/setup.html).

- (Not Recommended) Install [minconda](https://docs.conda.io/en/latest/miniconda.html).

- (Recommended) Install [miniforge](https://github.com/conda-forge/miniforge?tab=readme-ov-file) - recommended for this class

#### Setup SDS Environment
- Start -> Anaconda-> Anaconda Prompt. Under Anaconda Prompt window: 
- Create your own environment use - `conda create -n sds python=3.13`
- Activate your environment use conda - `conda activate sds`

#### To install Jupyterlab, under the Anaconda Prompt (Windows) or Terminal (MacOS/Linux), type
I suggest using mamba to install packages, it does the same thing as conda, but work much faster than conda. 
To install mamba: 
- conda install -n base -c conda-forge mamba

Now you can install Jupyter Lab using mamba:
- `mamba install -c conda-forge jupyterlab`

## Navigate the JupyterLab Environment

### Basic Dos command line
Check out this [link](https://www.computerhope.com/issues/chusedos.htm)

Open a Windows command line window by following the steps below:
Click `Start`, In the `Search` or `Run` line, type `cmd` (short for command), and press `Enter`.  The Windows command line should be shown. Typically, Windows starts you at your user directory.
Key tips 
- MS-DOS and the Windows command line are not case sensitive.
- The files and directories shown in Windows are also found in the command line.
- When working with a file or directory with a space, surround it in quotes. For example, the directory My Documents would be "My Documents" when typed.
- File names can have a long file name of 255 characters and a three-character file extension.
- When a file or directory is deleted in the command line, it is not moved into the Recycle Bin.
- 
If you need help with any of the command type /? after the command, here is a list of a few commonly used commands:
- Listing the files --  type `dir or dir –p' (page by page)
- Moving into a directory – type  `cd` command
- View the contents of a file – type  `start filename`
- Moving back a directory – type `cd ..` (going up), or `cd \users\wenge`
- Creating a directory – type `mkdir dirname`
- Switching drives--  type the letter of the drive:a colon, e.g. `d:` or `c:` and hit enter
- Creating a new file – `start filename`
- Moving and copying a file  -- `move file1 file2` or `copy file1 file2`
- Renaming a file – `rename f1 f2`
- Deleting a file – `del filename`
- Removing a directory – `rmdir dirname`
- Running a program – type the name of the executable file 
- How to list available commands – `help` 
- Closing or exiting the command line window – type `exit`


### Launch JupyterLab
- You  can start Jupyter Lab through Miniforge Prompt.window. For Window version: 
`Window Start Menu->Miniforge Prompt` to launch your minforge prompt, then type, 
`cd your working directory`
`Jupyter Lab` 
Hit enter, then you'll see the application opening in the web browser on the following address: http://localhost:8888.
Next time, when you login, repeat these steps again to start JupyterLab.  

### Close JupyterLab Environment
- If You start JupyterLab in the Terminal, find the terminal where JupyterLab is running, press `Ctrl + C (on macOS: Control + C)` once or twice. It will ask: Shutdown this Jupyter server (y/[n])? Type `y` and press Enter.

### Jupyter Lab Environment 
[Jupyter Lab](https://jupyterlab.readthedocs.io/en/latest/) is a web-based interactive development environment (IDE) for data science, coding, and documentation.JupyterLab enables you to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components in a flexible, integrated, and extensible manner.  
#### Characteristics of Jupyter Lab Environment
- Web-based interface: Runs in your browser, but executes code locally.
- Multi-document Layout: You can open multiple notebooks, terminals, text files, and plots side by side.
- Support multiple format files - Jupyter Notebook, images, CSV, JSON, Markdown, PDF, HDF5, Vega, Vega-Lite, LaTeX, and many more.
 - Kernel-based Execution: Code runs through kernels (e.g., Python). You can have multiple kernels running simultaneously. You can drag-and-drop to rearrange panels.
- Cross-Platform: Works on macOS, Windows, Linux — as long as you have Python installed.
- A brief [introduction to Jupyter Lab](https://youtu.be/A5YyoCKxEOU)

#### Two Main Components
- A kernel is a program that runs and introspects the user’s code. The Jupyter Notebook App has a kernel for Python code, but kernels are also available for other programming languages.

- The dashboard of the application not only shows you the notebook documents that you have made and can reopen, but can also be used to manage the kernels: you can see which ones are running and shut them down if necessary

### Jupyter Notebook Document 
[A Jupyter notebook](ttps://jupyter-notebook.readthedocs.io/en/latest/notebook.html) is a shareable document that combines computer code, plain language descriptions, data, rich visualizations like 3D models, charts, graphs and figures, and interactive controls. With like JupyterLab as an editor, it provides a fast interactive environment for prototyping and explaining code, exploring and visualizing data, and sharing ideas with others. 

#### Creating a New Notebook Document
A new notebook may be created anytime, either from the dashboard, or using the File ‣ New menu option from within an active notebook. The new notebook is created within the same directory and will open in a new browser tab. It will also be reflected as a new entry in the notebook list on the dashboard. 

#### Notebook User Interface
Once you open a new notebook, you see the notebook name, a menu bar, a toolbar and an empty code cell.![Data Science](img/notebook.png)

#### Structure of a Notebook Document
The notebook consists of a sequence of cells. A cell is a multiline text input field, and its contents can be executed by using Shift-Enter, or by clicking either the “Play” button in the toolbar, or Cell, Run in the menu bar. 

There are three types of cells: code cells, markdown cells, and raw cells. Every cell starts off being a code cell, but its type can be changed by using a drop-down on the toolbar (which will be “Code”, initially), or via keyboard shortcuts.

- **Code cells** allow you to edit and write new code, with full syntax highlighting and tab completion. The programming language you use depends on the kernel, and the default kernel (IPython) runs Python code

- **Markdown cells** allow you to document the computational process using descriptive rich texts. In IPython, this is accomplished by marking up text with the [Markdown language](https://www.markdownguide.org/getting-started/). When a Markdown cell is executed, the Markdown code is converted into the corresponding formatted rich text. Here is the [Markdown syntax](https://www.markdownguide.org/basic-syntax/) and a simple [Cheat Sheet](https://www.markdownguide.org/cheat-sheet/) to get you started.

- **Raw cells**  provide a place in which you can write output directly.The notebook does not evaluate raw cellsk

#### Keyboard Shortcuts
All actions in the notebook can be performed with the mouse, but keyboard shortcuts are also available and it can be convenient once you get familiar with them.
- `Shift-Enter`: run the current cell, show any output, and jump to the next cell below.
- `Ctrl-F`: find a text in the document
-  `Esc`: enter Command mode, you can use keyboard shortcuts: 
    - `a` → insert a cell above.
    - `b` → insert a cell below.
    - `c` → copy a cell.
    - `v` → paste a cell.
    - `x` → cut a cell.
    - `dd` → delete a cell. 
    - `z` → undo.
    - `shift + z` → redo.
    - Change the format of a cell
        - `m` → Markdown cell.
        - `y` → Code cell.
        - `r` → Raw cell.
- `Enter`: enter Edit mode, you can edit text in cells)

## Install Python Pacakges 
There are two basic approaches to installing Python packages
### Using pip (standard way)
- `pip install package_name`
- Prefer pip for general packages (wider availability).

### Using conda/mamba (if you use Anaconda/Miniconda)
- `mamba install pacakage_name` 
- `mamba install pandas` 
- `mamba install numpy`
- `mamba install matplotlib`
- `mamba install hvplot`


### References
* [Python Like You Mean It - module 1](https://www.pythonlikeyoumeanit.com/module_1.html)
* [Be ready for next week](https://www.pythonlikeyoumeanit.com/module_2.html)