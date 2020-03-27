---
title: "Tree Canopy Cover by Metro Area - Visualizing high-res geospatial data in Python"
date: 2020-03-18
categories:
  - Blog
tags:
  - Jekyll
  - update
header: 
  teaser: "/assets/images/tcc_preview.png"
---

*Blog post in progress* This blog illustrates how to render high-res geospatial data in Python, and investigates which urban areas have the highest and lowest urban tree cover.   
Measuring TCC is important for many reasons, including predicting electrical outages, modelling housing prices, and tracking climate change.  

Data Documentation, code, and instructions to reproduce this analysis are available on [my Github](https://github.com/zwrankin/blog/tree/master/tree_canopy_cover).  
I uploaded the processed data on [Kaggle Datasets](https://www.kaggle.com/zwrankin/usfs-tree-canopy-cover), including a [Notebook to run this analysis](https://www.kaggle.com/zwrankin/treecanopycover-starter)

## Background
Tree Canopy Cover (TCC) is a measure of the vegetation cover of an area. 
![](/assets/images/tcc/tcc_diagram.png)
Every 4 years, the USFS publishes TCC estimates for every 30x30 meter pixel in the United States. I downloaded the [2016 data](ttps://data.fs.usda.gov/geodata/rastergateway/treecanopycover/index.php) and compressed it to 1km pixels for ease of analysis. For background on TCC, see the [USFS Tree Canopy Cover brochure](https://data.fs.usda.gov/geodata/rastergateway/treecanopycover/docs/TCC_Tri-fold_2020-01-03.pdf)  


## Interactive visualization of high-density geospatial raster data in Python
[Folium](https://github.com/python-visualization/folium/tree/master/folium) is a popular Python library that combines the dynamic Leaflet geospatial library with the data manipulation prowess of Python.  Most visualizations using Folium use point data or choropleths (data tied to specific polygons). However, the TCC data has millions of pixels, which quickly overloads the normal Folium polygon functions. Fortunately, using the `folium.raster_layers.ImageOverlay` with the raw numpy matrix allows quick rendering while maintaining the interactive Leaflet tiles.  
This article will show how to use Folium raster layers to visualize high-resolution geospatial tree canopy cover data.  
[Click here](https://zanerankin.com/blog/tree_canopy_cover/output/map_tcc_usa_1km_city_overlay.html) for the interactive version of this map, including shapefiles.
![](/assets/images/tcc/tcc_map_preview.png) 

## Tree Canopy Cover by Metropolitan Area
City boundary shapefiles and census population data were downloaded from https://catalog.data.gov/dataset/500-cities-city-boundaries-acd62.  
TCC was aggregated within the boundaries of the 50 most populous cities, and analyzed in conjunction with derived population density.  
[Click here](http://zanerankin.com/blog/tree_canopy_cover/output/tcc_by_city_scatter.html) for the interactive version of this plot.  
![](/assets/images/tcc/tcc_scatter_preview.png)  

Take these rankings with a grain of salt. For example, here is the zoomed-in map of the highest tree-cover city, Raleigh. As you can tell, city boundaries are quite arbitrary. In this case, the inclusion of William B Umstead State Park in the city limits is certainly boosting the overall TCC value.  
![](/assets/images/tcc/tcc_raleigh.png)  
