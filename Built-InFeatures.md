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

# Advanced Editing

# Custom SVG Goodness

# Exporting Maps in SVG & PDF Format

# Databases

# Spatialite/Geopackage

# PostGIS
