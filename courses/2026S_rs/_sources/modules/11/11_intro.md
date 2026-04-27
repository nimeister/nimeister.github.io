# Lidar Remote Sensing - 1 

Starting from this week, we will learn lidar remote sensing. This unit includes four modules:
 
* Intro to lidar remote sensing
* lidar processing tools - LASTools and FUSION
* Lidar applications in vegetation - GEDI
* ICESat-2 mission 

## [Intro to lidar remote sensing](http://www.geography.hunter.cuny.edu/~wenge/GT322713_22S/lidar/lidar1_intro.pdf)

## Lidar data processing tools 
### [CloudCompare](https://www.cloudcompare.org/)

### [Lastools](https://rapidlasso.com/lastools/)
### [What can do with LASTools?](http://www.geography.hunter.cuny.edu/~wenge/GT322713_22S/lidar/LAStools1.pdf)
There is a complete listing of the tools in the bin folder and a _README.TXT file with each of the tools. Here’s a few examples:
* Project LAS files 
* Set the projection in the LAS/LAZ file header 
* Convert LAS files to a variety of formats including: Shapefiles and ASCII files 
* Filter points based on a variety of properties including: Classification,  Return, Scan Angle, and Bounding Box 
* Generate DEMs from LAS Files using any of the filtering options 
* Generate Rasters where the cell values represent the number of points that fall within the cell. 
* Export a LAS file to an X,Y,Z file TXT file that can be read into CAD systems 
* Generate a shapefile that represents the boundary of data within a LAS file 
* Compress LAS files up to 10 times turning a 400 megabyte LAS file into a 40 megabyte LAZ file 

### [How to get started with the LASTools](http://www.geography.hunter.cuny.edu/~wenge/GT322713_22S/lidar/NotefromMartinIsenburg.pdf)? 

### Run LASTools in command prompt: 

#### Install LASTools 
* Download LAStools.zip from this [link](https://rapidlasso.com/lastools/). 
* Unzip LASTOOLS to your C:\ drive and don’t put in a folder that has a space in the name. 
Simply taking the default and unzipping to the C:\ folder will result in a folder named “C:\LASTOOLS” 
and make sure you retain the folders that are included in the zip file. 
Unzipping will create a number of folders in this directory. 
All of the executable programs are stored in a folder named “c:\lastools\bin”. 
* It’s helpful to add the BIN folder to your system PATH environment variable (c:\lastools\bin). 
In the system search window, for example, for Window 10, go to Settings, then  search “env”, 
select “Edit environmental variables for your account”, 
in the “Environment Variables” window, click “Path”, then “Edit”. In the “Edit environmental variable”, 
click “New”, add “C:\LASTools” or the path you store LASTools, click “OK’. Now start the cmd tool window, 
type “lasview”
* [A easy way to run lastools](https://medium.com/@somegreg/installing-lastools-52204486831b)

### Basic Dos command line
Check out this [link](https://www.computerhope.com/issues/chusedos.htm)

Open a Windows command line window by following the steps below:
Click Start, In the Search or Run line, type cmd (short for command), and press Enter.  The Windows command line should be shown. Typically, Windows starts you at your user directory.
Key tips
- MS-DOS and the Windows command line are not case sensitive.
- The files and directories shown in Windows are also found in the command line.
- When working with a file or directory with a space, surround it in quotes. For example, the directory My Documents would be "My Documents" when typed.
- File names can have a long file name of 255 characters and a three character file extension.
- When a file or directory is deleted in the command line, it is not moved into the Recycle Bin.

If you need help with any of command type /? after the command, here is a list of a few commonly used commands:
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


### [Run Lastools in ArcGIS](https://www.youtube.com/watch?v=PaGK6zeSYzs&ab_channel=RamonArrowsmith)

### [Lastools in QGIS](https://www.geodose.com/2020/01/tutorial-lidar-data-processing-lastools-qgis.html)

## Lab11
* The goal of this lab is to get started with CloudCompare and Lastool and you can open and view a lidar dataset 
using lasview command and submit your screenshot of the lidar image you open. I put a lidar scene 
in //moon1/scratch/GTECH322-713/Lab_lidar/ or from this link: https://www.dropbox.com/scl/fi/odiahp90o8ttl2uicvs4h/BEF.zip?rlkey=zwz0n2coa6t2hipnt54f7y8cl&st=nukce327&dl=0 that you can use.  You can use your own lidar data. 