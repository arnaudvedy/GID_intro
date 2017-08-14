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
- To minimize setup time, we will be booting to a live OS in persistent mode. For this workshop we will be using [OSGEO Live](https://live.osgeo.org/en/index.html), as it already contains most of the tools needed for data analysis and spatial analysis. 
- Once OSGEO running, create a project folder in your `/home` directory:	
`mkdir gid-intro && cd gid-intro`
- Now download the latest GID dataset:	
`wget http://seshat.datasd.org/get_it_done_311/get_it_done_311_requests_datasd.csv`
- You are all set!

## 3. Exercise 1 -  Exploring GID data in a GIS environment
- We will start by opening the csv file in QGIS. Now, the file we have downloaded is not your typical geo-dataset in shapefile or geojson format. However, it contains `latitude` and `longitude` columns that we can take advantage of.

## 4. Exercise 2 - Exploring GID data in Python

## 5. What's next?
So you now have more context about Get It Done data 

What you should know as a developer:
- more formats are coming up
- more flexibility > API - there is already one, which only give you access to the latest reports.

