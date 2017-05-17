# Searching Existing Scripts
There are many existing **Scripts** in both **Python** and **R** for QGIS. You can find them by searching the web, but you can also browse many of them directly in QGIS through a tool similar to the **Plugin Manager**.

1. Open the **Processing toolbox**. Near the bottom you should see R scripts (If you've configured R) and Scripts (these are Python).
2. Under the Tools subitem, open "Get Scripts from on-line scripts collection"
3. In the dialog that opens you have 3 categories.
    1. In the **Not Installed** section you can browse and select algorithms with the check box. Note that you can check off many items. They will be installed once you push the OK button in the bottom right corner.
    2. To uninstall, go to the **Installed** section and uncheck. Once again, they won't uninstall until you press the OK button.
    3. If there is a newer version of the script it will list in the **Updatable** section and you'll be able to select.
4. Once installed the scripts are sorted into categories based on the metadata the author put in the script.

These scripts currently come from the [QGIS-processing repository](https://github.com/wildintellect/QGIS-Processing)

# Writing Scripts
You can write new scripts in either Python or R that can then be run from the toolbox or included in the Model Builder. The idea for these scripts is to do 1 simple task at a time. This way the scripts are more flexible and re-usable. If you have a more complicated process building a **Model** or **Plugin** might be a better way to go. If you need complex user interaction then a **Plugin** is a better choice.

Learn to [Write new Processing algorithms as python scripts](http://docs.qgis.org/2.14/en/docs/user_manual/processing/scripts.html#writing-new-processing-algorithms-as-python-scripts) Documentation for writing custom toolbox algorithms.

## Python & R

The same documentation for Python applies to R in term of defining inputs and outputs. The only major difference is that each language has it's own section in the toolbox.

Overview of [default R scripts](http://docs.qgis.org/2.14/en/docs/user_manual/processing_algs/r/index.html)

### Input & Output

Inputs and Outputs are defined before any code (they can be after comments). A double pound(##) signifies to Processing that these are inputs and outputs. Do not use elsewhere for comments in your script.

**Input**

You specify the name=type default

**Output**
If it's an output then it's
name=output type

See the [Processing Documentation](http://docs.qgis.org/2.14/en/docs/user_manual/processing/scripts.html) for all the allowed types and options.

Example
```
##Vector=group
##xmin=number -180
##xmax=number 180
##ymin=number -90
##ymax=number 90
##spacing=number 10
##density=number 1
##outfile=output file
##graticule=output vector
```
## Always make a help file
When you write a script file make a json file with the same filename and the extension .help in the same folder. The default path to the scripts is under the processing folder in your users' .qgis2 folder. ```Windows should be C:\Users\username\.qgis2/processing, Mac\Linux should be /home/user/.qgis2/processing```


The format for the file is {"keyname":"value","keyname2":"value2"}

The common predefined items are:

* "ALG_DESC"
* Input names and descriptions
* "ALG_CREATOR"
* Output names and descriptions
* "ALG_Version"
* "ALG_HELP_CREATOR"

Example
```
{"ALG_DESC": "Paragraph describing your algorithm. A backslash n is a new line\n Here's where you should mention additional libraries or packages users need to install like shapely(Python) or raster (R)\n In the next section you list each input and output variable and describe it's use and type.\n\n You can include html links: https://github.com/qgis/QGIS-Processing ", "var1": "Variable 1, a number","ALG_CREATOR": "Who wrote the script", "ALG_VERSION": "1", "ALG_HELP_CREATOR": "Who wrote the help"}
```

## Catalog your script into a group
The 1st double comment line (##), should be the GroupName you want to use equals group.
```
##Polygons=group
```

## Being careful
If your scripts require non-standard libraries(packages) to be installed in Python or R you should make sure your users know that. The help file is a good place to list those, along with a link on how to install python or R packages.

# Sharing Scripts

When you use the toolbox to download existing online scripts they come the [QGIS-processing repository](https://github.com/wildintellect/QGIS-Processing)

You can submit additional scripts on Github, by forking and doing a pull request. You can also directly share your scripts with other users. From a user perspective if you can download the script use the "Add script from file" to load it into your toolbox. Or just put them in your .qgis2/processing/scripts or rscripts folder and they will be detected.