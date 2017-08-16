# Workshop - Get It Done (GID)

## 1. Context
#### What is Get It Done?
![Get It Done](/img/gid-description.png)

#### Where do I retrieve GID data?
- Get it done data is available on the [City's open data portal](https://data.sandiego.gov). 
- You can either retrieve the entire dataset (all GID requests since launch in May 2016) 
- or a subset by problem category (e.g pothole, graffiti).

#### What does GID data look like?
- As of today, GID data is available in .csv format
- To have a better idea of what it actually looks like, you can actually preview it within the data portal or download the file and open it with your favorite spreadsheet editor.
- Quick overview of  columns

#### How is this data generated and how often is it updated?
- Thanks to our data automation system, [Poseidon](https://data.sandiego.gov/stories/why-data-automation-matters-data-portals/), the GID datasets are updated hourly. In other words, you always have access to the most recent data.
- Our data is generated as following:
![GID workflow](/img/poseidon.png)

## 2. Getting ready for the workshop
- To minimize setup time, we will be using a live OS in persistent mode. For this workshop we will be using [OSGEO Live](https://live.osgeo.org/en/index.html), as it already contains most of the tools needed for data analysis and spatial analysis. 
- Once OSGEO is up and running, open the terminal and retrieve this repo:	
	
`git clone https://github.com/arnaudvedy/GID_intro.git`

- You are all set!

## 3. Exercise 1 -  Exploring GID data in a GIS environment

### 3.1. Filter data and generate shapefile

- Launch QGIS	

`OS Launcher > Geospatial > Desktop GIS > QGIS`	

- Open the GID dataset	

`Layer > Add Layer > Add Delimited Text Layer` and open the `get_it_done_311_requests_datasd.csv` file from the `GID_intro/data` folder.

During this step you will need to specify the X and Y fields (longitude and latitude) and choose a coordinate system (wgs84).

- Open the city boundaries geoJSON dataset	

`Layer > Add Vector Layer` and open the `sd_boundaries.geojson` file from the `GID_intro/data` folder.

- Any obsevations at this point?
- Next, let's filter the data using the query builder `Ctrl + F` and the following expression: `"district" != ''`
- Export the filtered GID data to shapefile	

`Right click on layer in layer panel > Save as`	

Select ESRI Shapefile as format and save your file in the `/data` folder as  `gid.shp` 

### 3.2. Focus on a problem category

TBD

## 4. Exercise 2 - Exploring GID data in Python with Jupyter notebook

### 4.1. Jupyter notebook overview

- Open a terminal , navigate to your project folder (`~/GID_intro`), and type `jupyter-notebook`. This command should open the Jupyter web interface.
- What is Jupyter?
- What can you do with it?
- Why not just using Excel?
- Overview of the interface
- Next steps if you are into Jupyter notebooks.

### 4.2. Hello GID!

- Click on `New > Python 2 ` in the top-right corner of the interface
- Rename your notebook to whatever you want
- Let's write some python and explore how things work!

### 4.3. Notebook example

- First, open another terminal and install the plotly python package `pip install plotly`
- Using the Jupyter interface, open the `GID_intro.ipynb` file.


## 5. What's next?

- more data formats are coming up for 311 data
- more flexibility > API - there is already one, which only give you access to the latest reports.
- Other stuff

