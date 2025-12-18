# QGIS Plugin

The openEO QGIS plugin enables exploring openEO backends, collections, services  
within QGIS. The plugin can load the results of a job execution or web service to the QGIS map, so that the user can make further analyses and visualisation steps. Furthermore the plugin allows for display of collections, provided they are served as xyz or wmts tile map services.

## Installation
There are three different ways to install the QGIS Plugin:
 
1. The **latest stable version** is accessible in the plugin 
manager of QGIS (Plugins -> Manage and Install Plugins). Note that You have to activate the option to show experimental 
plugins (Settings -> Show also experimental plugins). After that, You can search for 
"OpenEO", install and activate the plugin.
2. The **github release version** is accessible on the 
[GitHub releases page](https://github.com/Open-EO/openeo-qgis-plugin/releases). First, download the zip archive. 
Next, open the plugin manager of QGIS (Plugins -> Manage and Install Plugins) and select "Install from ZIP". 
There You can browse for the downloaded zip archive, install and activate it.
3. The **latest version** (or a branch of Your choice) is accessible through the github repository [GitHub repository](https://github.com/Open-EO/openeo-qgis-plugin).
First, download or clone the repository.
Navigate inside the repository directory `cd openeo-qgis-plugin` and compress the plugin directory `openeo_plugin` as a `.zip` file
Use the steps outlined in 2. to install the plugin as a zip file.

After a successful installation and activation of the plugin, an openEO entry will be visible in the QGIS browser:

![QGIS Plugin Icon within the QGIS browser](./images/qgis_browser.png)

This is where all the functionality of the plugin in accessible.

## Connection

To connect to an openEO backend of Your choice, right-click the openEO browser entry and select "New openEO Connection".

This will open a dialog window that allows You to enter URL and name of Your new openEO connection or select a connection from [openEO Hub](https://hub.openeo.org/):

![QGIS Connection Dialog](./images/connection_dialog.png)

Now that You have chosen a backend, You can expand the openEO browser item and right-click on the connection entry to select "Log In (Authenticate)". This will allow You to use Basic authentication or [OpenID Connect](https://openid.net/connect/) authentication to login Your connection:

![QGIS Login Dialog](./images/login_dialog.png)

Using OpenID Connect login will open a window of Your system's web browser, where You are asked to authenticate Your connection.

If logged in successfully, next to **Collections**, it is now possible to expand the **Batch Job** and **Web Services** entry that can be found upon expanding Your connection browser item (provided the given backend supports each).

![Example of the sub-items of an openEO connection after successful login](./images/collections_items.png)

### Logging out

**IMPORTANT:** Basic login information and OpenID Connect tokens are stored in plain text within the settings of Your QGIS profile. On shared computers it is advised to log out of or remove connections after Your work is done in order to delete authentication information:

- **Right-click on connection** > **"Remove Connection"** or **"Log out"**

To remove all stored information on Your connections:

- **Right-click on openEO icon** > **"Remove all connections"** or **"Logout from all connections"**


## Exploring a backend
Upon connection to a backend, a list of all **Collections** provided by this backend is available. After authenticating this backend, lists for **Batch jobs** and **Web Services** that have been created by Your user account are available (as long as the backend supports the use of batch jobs or web services).
A **Detail** view of Your connection can be accessed via Right-click > "Details". This will open a web-browser that displays information on Your chosen backend.

### Collections
Expanding the Collections Sub-item will yield a list of all collections that are offered by Your openEO backend. 
using Right-click > "Details" will open a web-browser window that displays further information on Your selected collection.
Collections that have a tile-map-service available as a preview are displayed with a Raster-layer icon as opposed to the default cube icon. These Collections can be added as tile-map layers to Your project using either by Right-click > "Add Layer to Project" or by dragging the item from Your QGIS browser into Your QGIS map.

![Collections within the QGIS browser. Collections with an available preview have a checkerboard-icon whereas the default icon for a collection is cube shaped](./images/collections_list.png)

### Web Services

### Batch Jobs

#### Result Items

## Additional Information

* [Github Repository](https://github.com/Open-EO/openeo-qgis-plugin)
* [QGIS Plugin Page](https://plugins.qgis.org/plugins/openeo-qgis-plugin-master/)