# pga_splunk_app

# Overview
pga_sample_app is a sample Splunk application. Please, customize accordingly.

## Installation
To install splunk_sample_app, follow these steps:

Create a copy and apply a different name to the folder (recomended a intuitive name, i.e: PGA_security_monitoring or PGA_kubernetes_monitoring)
Edit $APP_HOME/default/app.conf file
Rename the label of your app (i.e: "label = PGA_security_monitoring" or PGA_kubernetes_monitoring)
Log in to your Splunk instance with an administrative account.
Navigate to the "Manage Apps" page.
Click on "Install app from file" and upload the app (i.e: "label = PGA_security_monitoring" or PGA_kubernetes_monitoring) package.

## Configuration
Access the app from the Splunk web interface.
Navigate to Settings > Knowledge > User Interface > Navigation menus > default 
Edit menus accordingly:

###Add dashboard on menu list
<view name=“dashboard_id" />

###Set default dashboard 
<view name=“dashboard_id" default='true' />

###Add link on menu list
<a href="https://dev.splunk.com/">Splunk Developer Portal</a>

###Add dashboards list as menu option
<collection label="All dashboards">
<view source="all" />
</collection>

###Add category list as menu option
<collection label="Dashboards (errors)">
<view source="all" match="error"/>
</collection>

## Default Folders and Their Uses

Here you will have the details of the files that should/can be in all folders.

### bin
Purpose: Contains executable scripts and binaries required by the app.
Usage: Place any Python scripts, shell scripts, or other executable files that your app needs to run here.
### default
Purpose: Contains default configuration files for the app.
Usage: Use this folder to store default configurations, such as props.conf, transforms.conf, inputs.conf, and other .conf files. Do not modify these files directly in a production environment; instead, override them in the local folder.
### local
Purpose: Contains local configuration files that override the default configurations.
Usage: Use this folder to store custom configurations specific to your deployment. Files in this folder override the corresponding files in the default folder.
### lookups
Purpose: Stores lookup tables used by the app.
Usage: Place CSV files or other lookup table files here. Define your lookups in transforms.conf and reference them in your searches.
### metadata
Purpose: Contains metadata information about the app, such as permissions.
Usage: Use default.meta and local.meta files to configure permissions and access controls for the app's objects.
### static
Purpose: Stores static assets like images, CSS, and JavaScript files.
Usage: Place static files required by the app's user interface in this folder.
### appserver
Purpose: Contains files for the app's web interface.
Usage: Use this folder for HTML files, web controllers, and other components that define the app's web interface.
### lib
Purpose: Contains third-party libraries and dependencies.
Usage: Place any external libraries or dependencies required by your app in this folder.
### readme
Purpose: Contains documentation and information about the app.
Usage: Use this folder to store README files, documentation, and other informative files for users.
ui
### nav
Purpose: Contains navigation bar configuration files.
Usage: Customize the navigation bar of the app here.
### views
Purpose: Stores XML view files for the app's dashboards.
Usage: Define and customize the app's dashboards and views in this folder.

