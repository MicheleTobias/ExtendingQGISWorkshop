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

# Advanced Editing & Digitizing for Vector Data
The Advanced Digitizing Toolbar provides advanced digitizing and editing tools for vector data.  You'll probably need to add the toolbar to be able to see it.  From the View menu, select Toolbars, then check the Advanced Digitizing Toolbar.  The QGIS User Manual has a [comprehensive discussion of what each of these tools can do](http://docs.qgis.org/2.14/en/docs/user_manual/working_with_vector/editing_geometry_attributes.html#advanced-digitizing).  QGIS Tutorials has a fairly comprehensive [tutorial on creating and editing vector data](http://www.qgistutorials.com/en/docs/digitizing_basics.html).

# Custom SVG Goodness
One of the exciting things about QGIS is the ability to make your own SVG markers and fills.  You can use any vector illustration software to make your own SVG files, but [Inkscape](https://inkscape.org) is an excellent open source program for creating vector image files.  The QGIS Training Manual has [instructions for making your own custom fills](http://docs.qgis.org/2.14/en/docs/training_manual/basic_map/symbology.html#hard-fa-creating-a-custom-svg-fill).  Anita Graser posted a [discussion of more symbol options](https://anitagraser.com/2016/10/23/more-icons-symbols-for-qgis/) including a plugin for sharing custom symbols.

# Exporting Maps in SVG & PDF Format
If you've used QGIS before, you're probably familiar with the Map Composer, the tool that lets you compose a map and then export it in an image format.  You may not have found a use for the PDF or SVG export yet.  The QGIS Training Manual walks you through [exporting an image, PDF, or SVG of a map](http://docs.qgis.org/2.14/en/docs/training_manual/map_composer/map_composer.html#basic-fa-exporting-your-map).

You can probably think of some reasons to export a PDF instead of an image file, but why do you want an SVG of a map anyway?  In the previous section, we introduced you to making custom map symbols in Inkscape, a vector illustration software.  SVG is the native file format for Inkscape, so you can save your map as an SVG, then hop on over to Inkscape to work on you map file a little more to clean it up, add in new elements, or combine output from other analysis programs like R.  Want even *MORE* about using Inkcape with QGIS for cartography?  Come to [FOSS4G 2017](http://2017.foss4g.org/) in Boston for Michele's workshop and talk, or watch her [2016 FOSS4G North America talk video](https://www.youtube.com/watch?v=tGNGEB7NetA), or check out her [YouTube Channel](https://www.youtube.com/user/MicheleTobias) which has some other fun things like a time-lapse video of a map coming together in Inkscape.

# Databases
