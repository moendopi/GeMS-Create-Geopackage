# GeMS-Create-Geopackage
A command line Python script to automatically create GeMS compliant GeoPackages for QGIS
*** For either of these scripts to run properly you need to install pygeopkg: pip install pygeopkg
Additionally, the crs_dictinoary.py, srs_dictionary.py, and GeMS_basic_feature_classes.py files need to be in the same folder as Create_GeMS_GeoPackage.py and/or Create_Full_GeMS_GeoPackage.py files to run properly.
Do not run this script in QGIS. As it stands it will not work trying to run the script in QGIS. The script prompts input which will cause the script to crash in QGIS. This can be run through an IDE like Visual Studio Code or Geanie, or you can run the script through a terminal session.
For Create_GeMS_GeoPackage
This script will prompt the user initially for 3 pieces of information: the path to store the GeoPackage once created a name for the GeoPackage, and a coordinate reference system number. Examples would include 26916 for NAD83 UTM Zone 16N or 32603 for WGS84 UTM Zone 3N.
Currently only NAD83 UTM Zones 1 - 20 and WGS84 UTM Zones 1 - 20 are available.
More information on coordinate reference systems can be found at https://spatialreference.org/.
Once the initial information is gathered the script will automatically create the GeoPackage and add the 5 basic feature classes required for a GeMS database: MapUnitPolys, ContactsAndFaults, and the three tables DescriptionOfMapsUnits, DataSources, and Glossary.
The user is then prompted to add additional optional feature classes. A list of feature classes is displayed. DO NOT ADD SPACES IN THE FEATURE CLASS NAME. DO NOT ADD SPACES. When you have entered all the desired feature classes, type done. The new features will be added to the GeoPackage.
If you prefer not to add any aadditional or optional feature classes just type done when prompted for optional feature classes.
For Create_Full_GeMS_GeoPackage This script will require the same three pieces of information from the user but will not prompt the user with any additional optional feature classes. It will instead just create a GeoPackage with all the defined GeMS Features (29 feature classes and tables).

