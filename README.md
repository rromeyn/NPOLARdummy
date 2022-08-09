# NPOLARdummy
Repository for trial exercises - antarctic glaciology
The background for this repository is an initial exploration of how to map icebergs near the calving front of ice shelves around the entire coastline of Antarctica.

# Description of Files

1 - DummySARprocessing.js
This is a JavaScript script containing Google Earth Engine commands that can be executed in a Google Earth Engine command window (although it is recommended to use the link in the code section below). The script contains an initial workflow to classify icebergs, sea ice and open water from Sentinel-1 imagery and export the segmentation result to geotiffs. Detailed description is provided in comments in the script.

2 - IceTypeLabelled_EPSG3857.tif
This is a single channel integer labelled geotiff image with pixel values of 1 for iceberg, 2 for sea ice and 3 for open water. The geotiff projection is Google pseudo-mercator (EPSG3857). The nominal pixel resolution of the image is 2000m and it covers the sector of the Antarctic coastline from ~70W to 15W. The integer labelled image would be the recommended product for further processing, but the segmentation result is poor at this initial stage so it should NOT be used for any operational purpose.

3 - IceTypeRGB_EPSG3857.tif
This is a 3-channel (RGB) geotiff image which provides a more convenient way to visualise the classification result than the single channel integer labelled image described above. Pixels classified iceberg are yellow (RGB 255,0,0), sea ice pixels are blue (RGB 0,0,255) and open water pixels are red (RGB 255,0,0). Masked pixels (background) are black (RGB 0,0,0). The geotiff projection is Google pseudo-mercator (EPSG3857). The nominal pixel resolution of the image is 2000m and it covers the sector of the Antarctic coastline from ~70W to 15W. Since this initial classification result is poor, this image should NOT be used for any operational purpose.

4 - InitialReport.pdf
This file contains a brief report on the initial exploratory phase of this project, aiming to study the calving of icebergs from ice shelves at up to the continental scale around the coastline of Antarctica. A small number of references to published studies are also given.

# Code

The Google earth engine code used to process Sentinel-1 data and export the classified geotiffs included in this repository can be executed using the following link (requires user to have a free Google Earth Engine account). The "raw" satellite data (orbit correction, border/thermal noise removal, radiometric calibration
and terrain correction are already applied) is hosted in the cloud on Google servers and the code also runs directly in the cloud on remote servers so the user only needs a basic computer with a web browser.

https://code.earthengine.google.com/e71e81ea79c88c95fd4c54fe30d880b9
