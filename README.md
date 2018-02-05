# Census-merged-wards

Split into census merged wards grouped by local authority into `.geojson` and `.topojson` filetypes.

Source is [ONS Geoportal](http://geoportal.statistics.gov.uk/datasets/e1ed938a33cf472fa802d99b1900164b_1). Dataset is Census Merged Wards (December 2011) Generalised Clipped Boundaries in England and Wales

Split by feature using QGIS
Load in the source shapefile.
![screen shot 2018-02-05 at 09 31 47](https://user-images.githubusercontent.com/2945099/35797599-17e6e53e-0a58-11e8-90f2-c30874506011.png)
Using the menu choose
Vector > Data management tools> Split vector layer. Choose lad11cd.
Choose the folder to save files.


[Batch convert to geojson](https://gist.github.com/benbalter/5858851). Add in the source projection `-s_srs EPSG:27700`. [Helpful tool](https://dragons8mycat.com/2014/04/29/gis-tips-how-to-find-the-epsg-code-of-your-shapefile/) to find out the projection of your shapefile.

[Batch convert to topojson](https://gis.stackexchange.com/questions/75561/batch-conversion-of-shapefiles-to-topojson) although they've changed the commands in topojson. You now need to use [`geo2topo`](https://github.com/topojson/topojson-server/blob/master/README.md#geo2topo)

Have included the scripts in this repo. Run the scripts in the folder with the terminal. E.g. Change directory into the folder and `./geojson-conversion.sh`.
