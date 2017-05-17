# Searching Existing Scripts
There are many existing **Scripts** in both **Python** and **R** for QGIS. You can find them by searching the web, but you can also browse many of them directly in QGIS through a tool similar to the **Plugin Manager**.

1. Open the **Processing toolbox**. Near the bottom you should see R scripts (If you've configured R) and Scripts (these are Python).
2. Under the Tools subitem, open "Get Scripts from on-line scripts collection"
3. In the dialog that opens you have 3 categories.
    1. In the **Not Installed** section you can browse and select algorithms with the check box. Note that you can check off many items. They will be installed once you push the OK button in the bottom right corner.
    2. To uninstall, go to the Installed section and uncheck. Once again, they won't uninstall until you press the OK button.
    3. If there is a newer version of the script it will list in the **Updatable** section and you'll be able to select.
4. Once installed the scripts are sorted into categories based on the metadata the author put in the script.

These scripts currently come from the [QGIS-processing repository](https://github.com/wildintellect/QGIS-Processing)

# Writing Scripts
You can write new scripts in either Python or R that can then be run from the toolbox or included in the Model Builder. The idea for this scripts is to do 1 simple task at a time. This way the scripts are more flexible and re-usable. If you have a more complicated process building a **Model** or **Plugin** might be a better way to go. If you need complex user interaction then a **Plugin** is a better choice.

Learn to [Write new Processing algorithms as python scripts¶](http://docs.qgis.org/2.14/en/docs/user_manual/processing/scripts.html#writing-new-processing-algorithms-as-python-scripts) Documentation for writing custom toolbox algorithms.

## Python & R

The same documentation for Python applies to R in term of defining inputs and outputs. The only major difference is that each language has it's own section in 

## Always make a help file
When you write a script file make a json file with the same filename and the extension .help

## Catalog your script into a group

## Being careful
If your scripts require non-standard functions or libraries to be installed in Python or R you should make sure your users know that. 

# Sharing Scripts

When you use the toolbox to download existing online scripts they come the [QGIS-processing repository](https://github.com/wildintellect/QGIS-Processing)

You can submit additional scripts on Github, by forking and doing a pull request. You can also directly share your scripts with other users. From a user perspective if you can download the script use the "Add script from file" to load it into your toolbox.