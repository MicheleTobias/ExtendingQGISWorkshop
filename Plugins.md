In this section, we'll learn about using existing plugins and briefly introduce the process of making your own plugins.

# Working with Plugins
## Using the Plugin Manager
Learn to use the Plugin Manager with [QGIS Tutorials & Tips' Using Plugins tutorial](http://www.qgistutorials.com/en/docs/using_plugins.html).

A tutorial from the [Module 10.1. Lesson: Installing and Managing Plugins](http://docs.qgis.org/2.14/en/docs/training_manual/qgis_plugins/fetching_plugins.html#basic-fa-configuring-additional-plugin-repositories) in the QGIS Training Manual covers similar topics.

## Finding Plugins
The number of plugins available for QGIS is growing.  How can you find what you're looking for?  The first option is to search inside the Plugin Manager.  Sometimes you find what you need that way, but it doesn't always turn up the best tool for the job.  Honestly (don't hate us for this answer) a Google search for "QGIS plugin" + the topic you're interested in is probably the best way.  From this, not only will you likely find the entry in the QGIS plugin list, but you'll find tutorials and posts related to any relevant plugins, including discussions of which option to pick if multiple options are available.  Additionally, you can search the [QGIS plugin list](http://plugins.qgis.org/plugins/).

## Try Some Plugins
We've picked out some plugins that we think are pretty useful.  We'd like you to try out a few plugins, just to get an idea of what's available and how they work.  You don't need to try all of these suggestions, but pick a couple and explore.  

|Plugin|Summary|Tutorial|
|---|---|---|
|QuickMapServices|Basemaps|[QuickMapServices: easy basemaps in QGIS](http://nextgis.com/blog/quickmapservices/) |
|Qgis2web|OpenLayers 3 and Leaflet webmaps from QGIS projects|[qgis2web wiki](https://github.com/tomchadwin/qgis2web/wiki) |
|QSpatiaLite| Work with Spatialite databases directly in QGIS |[Ecostudies Blog: New spatialite plugin for QGIS](https://pvanb.wordpress.com/2011/03/30/new-spatialite-plugin-for-qgis/) see also *QGIS 2 Cookbook* |
|TimeManager|Adds visualization for temporal geospatial data |[Anita Graser's Bird Migration Data Tutorial](https://anitagraser.com/2016/09/24/how-to-visualize-bird-migration-data-with-qgis-timemanager/) see also *QGIS 2 Cookbook* |
|TableManager|Edit attribute table column names and order |[Honey Bee Research Association's Table Manager Tutorial](http://www.coloss.org/beebook/I/gis/7/4/5/2) |
|QGIS Resource Sharing| Share and Download sets of SVG icons | [More icons & symbols for QGIS](https://anitagraser.com/2016/10/23/more-icons-symbols-for-qgis/) |
|DigitizingTools| Additional tools useful when digtizing vector data |[Digtizing Tools Usage Wiki Page](https://github.com/bstroebl/DigitizingTools/wiki/Usage) |
|Numerical Vertex Edit| Enter coordinates by hand or move points to exact coordinates | [GIS Lounge: How to Map a Single Set of Coordinate Using QGIS](https://www.gislounge.com/map-single-coordinate-using-qgis/)|
|Numerical Digitize| Digitize points with coordinates |[Geospatial Solutions Expert: How to Plot a Single Set of Point Coordinate in an existing layer Using QGIS](https://umar-yusuf.blogspot.com/2016/06/How-to-Plot-a-Single-Set-of-Point-Coordinate-in-an-existing-layer-Using-QGIS.html) |

Feeling adventurous? Try searching for a plugin topic of interest to your work and give it a try!

### Lot's of plugins on the same topics

If you recall Data-defined labelling from [Built-In Features](https://github.com/MicheleTobias/ExtendingQGISWorkshop/blob/master/Built-InFeatures.md)
There are actually 3 great plugins that make it even easier:

* Create labeled layer - Create a shapefile with fields configured for labelling
* EasyCustomLabeling - Copy a layer to a memory layer with fields configured for labelling
* Layer to labeled layer - Add fields configured for labelling

### Dont' forget about Experimental Plugins

The authors of plugins have an option to release experimental plugins. These tend to be slightly less polished but often work just the same, and many authors encourage bug reports. You have to specifically enable Experimental plugins in the plugin manager to be able to install them.

## Managing Plugins
Loaded plugins take a lot of memory, which adds to the program start time, occasionally causes crashes, or rarely can cause conflicts of software versions.  For these reasons, turn off plugins that you are not using.  Given that you've just tried a bunch of new plugins it would be a good time to visit the Plugin Manager to turn off any that you don't think you'll be using on a regular basis.

# Making New Plugins
Writing your own python or c++ plugins for QGIS can easily be it's own workshop, if not a full course, so we'll just introduce the general concepts here.  We encourage you to explore this concept more if it is of interest to you.  Both of your instructors have experience with this topic, so please ask us questions if you'd like to know more.

The PyQGIS Cookbook has a good introduction to [Developing Python Plugins](http://docs.qgis.org/testing/en/docs/pyqgis_developer_cookbook/plugins.html).  Entertainingly, there is a QGIS plugin called [QGIS Plugin Builder](http://geoapt.net/pluginbuilder/) with tools and excellent documentation to help you write QGIS plugins.
