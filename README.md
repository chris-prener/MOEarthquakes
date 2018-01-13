# MOEarthquakes

### Introduction
This repository has two goals. One, it provides an example of the project directory structure that is discussed in [Chapter 4](https://chris-prener.github.io/SSDSBook/organizing-projects.html) of [Sociospatial Data Science](https://chris-prener.github.io/SSDSBook). Two, it provides working examples of a number of key skills for sociospatial data science:

* accessing spatial data via [`tigris`](https://cran.r-project.org/web/packages/tigris/index.html)
* cleaning and geoprocessing spatial data with [`dplyr`](http://dplyr.tidyverse.org) and [`sf`](https://r-spatial.github.io/sf/)
* exploring patterns in spatial data [`ggplot2`](http://ggplot2.tidyverse.org) and [`RColorBrewer`](https://cran.r-project.org/web/packages/RColorBrewer/index.html)

### `ggplot2` Note
The CRAN release of `ggplot2` does not include the `geom_sf()` geom for plotting simple features. This tutorial therefore requires the [development version](https://github.com/tidyverse/ggplot2), which you can install from GitHub using the `devtools` package. 

### Sample Output
The `MOEarthquakes.Rmd` notebook creates a shapefile of earthquakes in Missouri between 1973 and 2017 that were at least 2.0 on the [Richter scale](https://en.wikipedia.org/wiki/Richter_magnitude_scale). These data can be [previewed in this repository](/results/GEO_Earthquakes.geojson).
