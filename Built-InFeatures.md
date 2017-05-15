QGIS has a **ton** of built-in features that you may not find on your own.

# File Formats
QGIS can read and write in a vast array of formats.  You're already familiar with the shapefile, but we'll recommend you look at a few others that may be less familiar.

## Geopackage
Geopackage is an excellent format for vector data exchange.  It's an open format and is readable by QGIS, ArcGIS, and presumably other geospatial programs since it has been incorporated into GDAL.  Geopackage can also store raster data, but given that it limits data to 3 bands for JPG or 4 (RBG + alpha) for PNG, we'd recommend GeoTIFF for most of your raster exchange needs.

## GeoTIFF
GeoTIFF is great for exchanging raster data.  It can store and unlimited number of bands (as compared with 3 for rasters in the Geopackage format), as well as "no data" cells.  It is also incorporated into GDAL.

## GeoJSON
GeoJSON is a single-file vector format that human-readable with a text editor and has a structure similar to XML.  Added bonus: GitHub will automatically visualize GeoJSON files in online repositories!

# Rule-Based Styles
Rule-based styles allow you to combine the power of an SQL-style query with the visualization capabilities of QGIS.  Have a road layer and want the highways to display differently than the surface streets?  This is your tool!  Nathan Woodrow has a [tutorial on using the rule-based style renderer](https://nathanw.net/2011/06/06/one-of-my-favorite-features-of-qgis/).

# Advanced Editing

# Custom SVG Goodness
One of the exciting things about QGIS is the ability to make your own SVG markers and fills.  You can use any vector illustration software to make your own SVG files, but [Inkscape](https://inkscape.org) is an excellent open source program for creating vector image files.  The QGIS Training Manual has [instructions for making your own custom fills](http://docs.qgis.org/2.14/en/docs/training_manual/basic_map/symbology.html#hard-fa-creating-a-custom-svg-fill).  Anita Graser posted a [discussion of more symbol options](https://anitagraser.com/2016/10/23/more-icons-symbols-for-qgis/) including a plugin for sharing custom symbols.

# Exporting Maps in SVG & PDF Format

# Databases
