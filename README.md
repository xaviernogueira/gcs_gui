## Geomorphic Covariance Structure (GCS) analysis GUI

### Package contents
- Graphic user interface executable script (gcs_gui.py)
- Python files defining GUi implemented function/methods
- Copy of RapidLasso's LAStools software (http://lastools.org/)
- Copy of 'Breeze' GUI theme (https://github.com/MaxPerl/ttk-Breeze)

### Pre-requisite packages
- arcpy (+ Spatial Analyst licence)
-- Comes with ArcGIS Python 3 default environment. 
  Clone environment to enable external package installation. 
- pillow (https://python-pillow.org/)
- plotly (https://plotly.com/)
- seaborn (https://seaborn.pydata.org/)

### Setting up -- Create a folder containing following:
- LAS/LAZ point cloud data files with spatial extents/footprint that
  capture a river valley's in-channel topography. 
  - Either bathymetric LiDAR or traditional LiDAR collected during dry channel conditions.
- Any shapefile (.shp) from the LiDAR project's metadata that has a spatial reference frame matching the point cloud data.
  - Can also be manually created based on project metadata files.
- A shapefile (.shp) defining the analysis area of interest (AOI).
  -   Projected in a spatial reference frame with desired analysis units (Meters 
      or US Feet)This shapefile's spatial reference is applied to all output  files.
- A folder (within the top level directory) containing only 4-band NAIP imagery .jp2 files that cover the AOI. 


### Literature 
This package applies a GCS analysis that has been refined over the
past decade. The applied methodology is described in  detail, as well as linked to known hydro-
morphodynamic fluvial mechanisms, within the following publications (in chronological order):
- MacWilliams, M. L., Wheaton, J. M., Pasternack, G. B., Street, R. L., &amp; Kitanidis, P. K.
(2006). Flow convergence routing hypothesis for pool-riffle maintenance in alluvial
rivers. Water Resources Research, 42(10), 1–21.
https://doi.org/10.1029/2005WR004391
   

- Wyrick, J. R., &amp; Pasternack, G. B. (2016). Revealing the natural complexity of topographic
change processes through repeat surveys and decision-tree classification. Earth Surface
Processes and Landforms, 41(6), 723–737. https://doi.org/10.1002/esp.3854
  

- Brown, R. A., &amp; Pasternack, G. B. (2017). Bed and width oscillations form coherent
patterns in a partially confined, regulated gravel-cobble-bedded river adjusting to
anthropogenic disturbances. Earth Surface Dynamics, 5(1), 1–20.
https://doi.org/10.5194/esurf-5-1-2017
  

- Pasternack, G. B., Baig, D., Weber, M. D., &amp; Brown, R. A. (2018a). Hierarchically nested
river landform sequences. Part 1: Theory. Earth Surface Processes and Landforms,
43(12), 2510–2518. https://doi.org/10.1002/esp.4411
  

- Pasternack, G. B., Baig, D., Weber, M. D., &amp; Brown, R. A. (2018b). Hierarchically nested
river landform sequences. Part 2: Bankfull channel morphodynamics governed by
valley nesting structure. Earth Surface Processes and Landforms, 43(12), 2519–2532.
https://doi.org/10.1002/esp.4410

For those without access to  journal publications, or looking for a synopsis of the pertinent
literature, a YouTube video by Gregory Pasternack (Ph.D) is available: https://www.youtube.com/watch?v=yvikf8C8Fxs


## Using the GUI
The GUI has seven tabs, each enabling different segments of the GCS analysis methodology.
The tabs are designed to be ran sequentially, and in some cases require manual inputs or inspection between them.
The outputs of a step/tab are typically the inputs of the next one. Do not alter the file
structure that is automatically generated by this package, as this can introduce errors or bugs.
The sections below describe the goals, inputs, outputs, and user requirements associated with each step of the analysis.
Different user choices can effect the final analysis results in relevant ways, therefore we recomended referencing this
guide prior to any choosing parameters or manually editing shapefiles.


#### Tab 1 -- Prepping LiDAR data from processing
Overview:

Inputs:

NDVI value selection

Outputs: 
#### Tab 2 -- Generating a ground-surface DEM from LiDAR data
#### Tab 3 -- Generating a thalweg centerline + elevation profile
#### Tab 4 -- Thalweg based DEM detrending
#### Tab 5 -- Selecting key flow stage heights + refining center-lines 
#### Tab 6(1) -- Running key flow stage GCS analysis
#### Tab 6(2) -- Interpreting output statistics and plots
#### Tab 7 --  Exporting GCS to River Builder

## Interpreting results