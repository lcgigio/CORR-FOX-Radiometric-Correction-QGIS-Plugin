<img width="3456" height="2115" alt="icon" src="https://github.com/user-attachments/assets/4679425f-cdf6-4ee1-b786-e8606e65adad" />

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23603097.svg)](https://doi.org/10.5281/zenodo.23603097)

The Corr. FOX plugin was designed to perform radiometric band calibration in QGIS, specifically tailored for multispectral cameras mounted on _drones_, Unmanned Aerial Vehicle (UAV) or Remotely Piloted Aircraft (RPAs) and field calibration panels, utilizing the Empirical Line method.

**Primary Goal:** To convert Digital Number (DN) images into absolute reflectance values (ranging from 0.0 to 1.0) based on known ground calibration targets, such as calibration panels or homogeneous surfaces.

**Standard Workflow:**

<img width="1920" height="1080" alt="UAV Bands (2)" src="https://github.com/user-attachments/assets/7c0cd16b-f742-4198-9ab8-b2d46d78f115" />

**Setup:** Link the raster images to their corresponding bands or select the directory where the files are stored.

**Mark targets on the plates:** Use the interactive tools to delineate the calibration panels/targets directly on the map. Each plates must be delineated on the images using polygons, from which the mean values are extracted as Digital Numbers (DN). 

<img width="1217" height="977" alt="sampling" src="https://github.com/user-attachments/assets/aaca2422-f79a-4a0a-ba90-743b0f2b430d" />


**Regression:** The statistics obtained from the image bands are extracted as Digital Number (DN) values. The mean DN value of each panel, together with its corresponding reflectance value obtained in the field, is used to generate linear regression equations for each input band. These regressions can be fitted either with an intercept ($\rho_{sup} = a \cdot DN + b$) or forced through the origin ($b = 0$).


<img width="1169" height="912" alt="reflectance" src="https://github.com/user-attachments/assets/549bb06c-38b5-4bce-9408-7cac67b46e65" />


**Calibration:** Execute each of the band-specific equations and generate the newly corrected raster layers directly within your project.

**Export:** Save your visual reports (PDF) alongside your tabular and spatial data (CSV/SHP).
