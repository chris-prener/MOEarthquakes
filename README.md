# MOEarthquakes

## Introduction
This repository has two goals. One, it provides an example of the project directory structure that is discussed in [Chapter 4](https://chris-prener.github.io/SSDSBook/organizing-projects.html) of [Sociospatial Data Science](https://chris-prener.github.io/SSDSBook). This is an extension of the project organization strategy by Greg Wilson, [Jenny Bryan](https://github.com/jennybc), and colleagues in their excellent article [*Good enough practices in scientific computing*](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510).

Two, it provides working examples of a number of key skills for sociospatial data science:

* accessing spatial data via [`tigris`](https://cran.r-project.org/web/packages/tigris/index.html)
* cleaning and geoprocessing spatial data with [`dplyr`](http://dplyr.tidyverse.org) and [`sf`](https://r-spatial.github.io/sf/)
* exploring patterns in spatial data [`ggplot2`](http://ggplot2.tidyverse.org) and [`RColorBrewer`](https://cran.r-project.org/web/packages/RColorBrewer/index.html)
* creating interactive maps using [`leaflet`](https://rstudio.github.io/leaflet/)

## Seismic Activity in Missouri
Missouri is an interesting state for mapping earthquakes due to the presence of the [New Madrid seismic zone](https://en.wikipedia.org/wiki/New_Madrid_Seismic_Zone) in the southeast part of the state (known as the "bootheel"). The region was the site of a [series of powerful earthquakes](https://en.wikipedia.org/wiki/1811–12_New_Madrid_earthquakes) in 1811 and 1812 near [New Madrid, MO](https://en.wikipedia.org/wiki/New_Madrid,_Missouri). These earthquakes have been estimated to be the [most powerful ones](https://en.wikipedia.org/wiki/List_of_earthquakes_in_the_United_States) to occur east of the Rocky Mountains in recorded history. This area was also rated by the USGS in 2014 as having some of the highest earthquake hazard levels in the continental United States east of the Rocky Mountains:

![](https://earthquake.usgs.gov/hazards/hazmaps/conterminous/2014/images/HazardMap2014_lg.jpg)

## Progression
There are four notebooks included in the `doc` subdirectory. The intended progression through these notebooks is as follows:

1. `CreateQuakes.Rmd` - initial creation of a shapefile containing earthquakes in Missouri
2. `ExploreQuakes.Rmd` - exploratory data analysis and mapping of the earthquake data
3. `CountyQuakes.Rmd` - additional mapping of earthquakes by county
4. `LeafletQuakes.Rmd` - creation of an interactive maps of both the point and county earthquake data

## `ggplot2` Note
The CRAN release of `ggplot2` does not include the `geom_sf()` geom for plotting simple features. This tutorial therefore requires the [development version](https://github.com/tidyverse/ggplot2), which you can install from GitHub using the `devtools` package.

## Sample Output
The `CreateQuakes.Rmd` notebook creates a shapefile of earthquakes in Missouri between 1973 and 2017 that were at least 2.0 on the [Richter scale](https://en.wikipedia.org/wiki/Richter_magnitude_scale). These data can be [previewed in this repository](/results/GEO_Earthquakes/GEO_Earthquakes.geojson).

## Want to do this for a different state?
Since this is a part of my [Introduction to GIS course](https://slu-soc5650.github.io) and I teach at a university in St. Louis, we focus on Missouri. However, it would be relatively easy to replicate this set of exercises with data from another state. `CreateQuakes.Rmd` contains a description of how the raw data were obtained. This process would need to be done again, with a custom geographic area defined around your state of interest. The `tigris` functions in `CreateQuakes.Rmd` and `CountyQuakes.Rmd` would also have to be adjusted.
