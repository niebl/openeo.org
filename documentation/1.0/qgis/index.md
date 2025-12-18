# QGIS Plugin

The openEO QGIS plugin enables exploring openEO backends, collections, services  
within QGIS. The plugin can load the results of a job execution or web service to the QGIS map, so that the user can make further analyses and visualisation steps. Furthermore the plugin allows for display of collections, provided they are served as xyz or wmts tile map services.

## Installation
There are three different ways to install the QGIS Plugin:
 
1. The **latest stable version** is accessible in the plugin 
manager of QGIS (Plugins -> Manage and Install Plugins). Note that you have to activate the option to show experimental 
plugins (Settings -> Show also experimental plugins). After that, you can search for 
"OpenEO", install and activate the plugin.
2. The **github release version** is accessible on the 
[GitHub releases page](https://github.com/Open-EO/openeo-qgis-plugin/releases). First, download the zip archive. 
Next, open the plugin manager of QGIS (Plugins -> Manage and Install Plugins) and select "Install from ZIP". 
There you can browse for the downloaded zip archive, install and activate it.
3. The **latest version** (or a branch of your choice) is accessible through the github repository [GitHub repository](https://github.com/Open-EO/openeo-qgis-plugin).
First, download or clone the repository.
Navigate inside the repository directory `cd openeo-qgis-plugin` and compress the plugin directory `openeo_plugin` as a `.zip` file
Use the steps outlined in 2. to install the plugin as a zip file.

After a successful installation and activation of the plugin, an openEO entry will be visible in the QGIS browser:

![QGIS Plugin Icon within the QGIS browser](./images/qgis_browser.png)

This is where all the functionality of the plugin in accessible.

## Connection

To connect to an openEO backend of your choice, right-click the openEO browser entry and select "New openEO Connection".

This will open a dialog window that allows you to enter URL and name of your new openEO connection or select a connection from [openEO Hub](https://hub.openeo.org/):

![QGIS Connection Dialog](./images/connection_dialog.png)

Now that you have chosen a backend, you can expand the openEO browser item and right-click on the connection entry to select "Log In (Authenticate)". This will allow you to use Basic authentication or [OpenID Connect](https://openid.net/connect/) authentication to login your connection:

![QGIS Login Dialog](./images/login_dialog.png)

Using OpenID Connect login will open a window of your system's web browser, where you are asked to authenticate your connection.

If logged in successfully, next to **Collections**, it is now possible to expand the **Batch Job** and **Web Services** entry that can be found upon expanding your connection browser item (provided the given backend supports each).

![Example of the sub-items of an openEO connection after successful login](./images/collections_items.png)

## Exploring a backend
