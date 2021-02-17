# OCF_PVmapper
PVmapping for the Open Climate Fix nonprofit

Files:

* Exploratory_Data_Analysis.ipynb: Notebook that explores images, makes cutouts for labelling, reads in json lables, converts to geojsons and updates binary maps
* Create_cutouts.ipynb: Notebook that generates numerous useful geojsons, samples points within and outside panels, create image and binary cutouts to train on
* data:
  * Exeter_tiles_orig.geojson: Polygons of each image tile
  * Exeter_tiles_union.geojson: Union of all image tiles
  * all_panels.geojson: Polygons of all panels
  * all_panels_buffer.geojson: above but with buffer (so as not to include panels within negative cutouts)
  * buffered_tiles.geojson: Same as Exeter_tiles_orig.geojson but with buffer so cutouts do not hit boundary of images
  * buffered_tiles_intersect.geojson: Interscetion of above (i.e. areas we can sample in to avoid image boundaries)
  * negative_mask.geojson: Negative mask from which to sample cutout centres
  * positive_mask.geojson: Positive mask from which to sample cutout centres
  * neg_samples.geojson: Centre points of negative samples
  * pos_samples.geojson: Cetnre poits of positive samples
  
* Example_Deepnet.ipynb: Google Colab notebook for reading in and saving cutouts as tensorflow records (to Google cloud storage)
* Deepnet_model1.ipynb: Google Colab notebook for running first (simple) image segmentation model
  
