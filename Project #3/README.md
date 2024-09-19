# Data Directories

## raw  

- The original datasets with ground truth values is pulled from https://easy.dans.knaw.nl/ui/rest/datasets/easy-dataset%3A158308. It contains 10 L1C atmospherically corrected (Sen2Cor) Sentinel2 images taken during September 2018.
Size of each image is 800x800 px. Each image is a multi-spectral image with RGB + NI channels.
  
- Data for other months (February and April) is fetched from https://scihub.copernicus.eu/dhus/#/home. Exact granule is T31UFU.
## processed  

- Based on ground truth images two separate ground truths were created. One for line ground truth, and the other for field ground truth (parcel segment). Ground truth and input images are cut in 56x56 px patches.

- For data fetched from scihub - RGB and NI channels are merged into a virtual tile in QGIS and a script is run to create 56x56 px image patches (located in raw folder) .
