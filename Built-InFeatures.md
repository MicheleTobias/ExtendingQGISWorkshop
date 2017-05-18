QGIS has a **ton** of built-in features that you may not find on your own.

# File Formats
QGIS can read and write in a vast array of formats.  You're already familiar with the shapefile, but we'll recommend you look at a few others that may be less familiar.

## Geopackage
Geopackage is an excellent format for vector data exchange.  It's an open format and is readable by QGIS, ArcGIS, and presumably other geospatial programs since it has been incorporated into GDAL.  Geopackage can also store raster data, but given that it limits data to 3 bands for JPG or 4 (RBG + alpha) for PNG, we'd recommend GeoTIFF for most of your raster exchange needs.

## GeoTIFF
GeoTIFF is great for exchanging raster data.  It can store and unlimited number of bands (as compared with 3 for rasters in the Geopackage format), as well as "no data" cells.  It is also incorporated into GDAL and supports lossless compression.

## GeoJSON
GeoJSON is a single-file vector format that's human-readable with a text editor and has a structure similar to XML, but is more efficient (less text = smaller file sizes). It's a variant of the common web exchange format JSON. Added bonus: GitHub will automatically visualize GeoJSON files in online repositories!

### TopoJSON
Keep an eye out for support of TopoJSON, GeoJSON with topology to reduce the redundancy of shared nodes.

# Data-defined Labels
Data defined labels allow you to style, place and orient your labels based on values in your attribute table. These properties can be hand edited, with the changes recorded to the table. It the best of both worlds, automated labelling with custom overrides, without the need to split the labels to another layer or content type (Annotations). This system can be used to create Annotation type layers, but one's that behave just like other vector layers, editing, browsing, updating by script or calucalation, batch changes, etc... *Insert link to tutorial here*

# Rule-Based Styles
Rule-based styles allow you to combine the power of an SQL-style query with the visualization capabilities of QGIS.  Have a road layer and want the highways to display differently than the surface streets?  This is your tool!  Nathan Woodrow has a [tutorial on using the rule-based style renderer](https://nathanw.net/2011/06/06/one-of-my-favorite-features-of-qgis/).

To skip to a more complicated example of using rule based styling follow Anita Grasers' [A guide to GoogleMaps-like maps with OSM in QGIS](https://anitagraser.com/2014/05/31/a-guide-to-googlemaps-like-maps-with-osm-in-qgis/)

# Advanced Editing & Digitizing for Vector Data
The Advanced Digitizing Toolbar provides advanced digitizing and editing tools for vector data.  You'll probably need to add the toolbar to be able to see it.  From the View menu, select Toolbars, then check the Advanced Digitizing Toolbar.  The QGIS User Manual has a [comprehensive discussion of what each of these tools can do](http://docs.qgis.org/2.14/en/docs/user_manual/working_with_vector/editing_geometry_attributes.html#advanced-digitizing).  QGIS Tutorials has a fairly comprehensive [tutorial on creating and editing vector data](http://www.qgistutorials.com/en/docs/digitizing_basics.html).

# Custom SVG Goodness
One of the exciting things about QGIS is the ability to make your own SVG markers and fills.  You can use any vector illustration software to make your own SVG files, but [Inkscape](https://inkscape.org) is an excellent open source program for creating vector image files.  The QGIS Training Manual has [instructions for making your own custom fills](http://docs.qgis.org/2.14/en/docs/training_manual/basic_map/symbology.html#hard-fa-creating-a-custom-svg-fill).  Anita Graser posted a [discussion of more symbol options](https://anitagraser.com/2016/10/23/more-icons-symbols-for-qgis/) including a plugin for sharing custom symbols.

# Exporting Maps in SVG & PDF Format
If you've used QGIS before, you're probably familiar with the [Print Composer](http://docs.qgis.org/2.18/en/docs/user_manual/print_composer/index.html), the tool that lets you compose a map and then export it in an image format.  You may not have found a use for the PDF or SVG export yet.  The QGIS Training Manual walks you through [exporting an image, PDF, or SVG of a map](http://docs.qgis.org/2.14/en/docs/training_manual/map_composer/map_composer.html#basic-fa-exporting-your-map).

You can probably think of some reasons to export a PDF instead of an image file, but why do you want an SVG of a map anyway?  In the previous section, we introduced you to making custom map symbols in Inkscape, a vector illustration software.  SVG is the native file format for Inkscape, so you can save your map as an SVG, then hop on over to Inkscape to work on you map file a little more to clean it up, add in new elements, or combine output from other analysis programs like R.  Want even *MORE* about using Inkcape with QGIS for cartography?  Come to [FOSS4G 2017](http://2017.foss4g.org/) in Boston for Michele's workshop and talk, or watch her [2016 FOSS4G North America talk video](https://www.youtube.com/watch?v=tGNGEB7NetA), or check out her [YouTube Channel](https://www.youtube.com/user/MicheleTobias) which has some other fun things like a time-lapse video of a map coming together in Inkscape.

# Databases
QGIS integrates natively with spatial databases like Spatialite and PostGIS.  Why does this matter?  It means you can store all your data for one project in a single database rather than managing a number of files (sometimes multiple files for one dataset... I'm looking at you, shapefile!) and not have to move them around to work with them.  For those familiar with GRASS' mapset and location concept, this might feel similar, but spatial databases are a refinement to these concepts.  Because many GIS people are visual learners and understand things better if they can see them, learning to work with a database with no visualization capability built-in can be daunting or just down-right unappealing.  Connecting your databse to QGIS allows you to visualize the results of queries which can help visual learners understand the results they create.

To work through many of the database tutorials, you'll actually need to install the database software and import some spatial data to work with in QGIS.  This is a lot to do for a 4-hour workshop like this (working with spatial databses can really be it's own workshop), so we'll encourage you to skim the tutorials we're about to mention and come back to try them out later when you have more time to focus on it.  If you've already got a Spatialite or PostGIS database set up, you may not have tried connecting it yet to QGIS.  Now's a great time to give that a try.

The QGIS Training Manual has several tutorials we'd recommend:
1. [Database Concepts with PostgreSQL](http://docs.qgis.org/2.14/en/docs/training_manual/database_concepts/index.html)
2. [Spatial Databse Concepts with PostGIS](http://docs.qgis.org/2.14/en/docs/training_manual/spatial_databases/index.html)
3. [Using Spatial Databases in QGIS](http://docs.qgis.org/2.14/en/docs/training_manual/databases/index.html)

Working with Spatialite layers in QGIS is very similar to how you work with PostGIS layers.
