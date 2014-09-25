WASP
====

Watershed Annotation and Segmentation Plugin for 3D Slicer

The plugin consists of two main components

* Watershed stage: Perform a series of watershed filters on the original image
* Annotation stage: Creating a new label map out of selected components from the watershed stage

Watershed stage
----

It allows the user to perform a series of Watershed segmentations on a 3D image using the SimpleITK “Morphological Watershed” without seeds. 

They can edit various parameters but importantly they can choose a range of values to use for the “watershed level”. 

* When the watershed value is lower the image will be segmented into more components. 
* When the watershed level is higher the image will be segmented into less components

A user can then use a range for this parameter (e.g. 1 to 2 with steps of 0.1 resulting in 20 label map results)

Annotation stage
----

The user can then select individual segmentations out of any of the watershed produced label map using fiducials.

This will create a new label map with only the components the user has chosen. The user can also choose the order of the labels as well.

A model of the label map is generated as well. 
