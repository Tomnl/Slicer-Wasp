WASP
====

Watershed Annotation and Segmentation Plugin for 3D Slicer

The plugin consists of two main components

* Watershed stage: Perform a series of watershed filters on the original image
* Annotation stage: Creating a new label map out of selected components from the watershed stage

NOTE: There has been a change in one of the core modules for Slicer. Some small changes in the WASP code were made to accommodate this.

I have tested the nightly version Slicer-4.4.0-2015-07-10-linux-amd64 and it seems to work fine.

If you are using the stable 4.4.0 version then use the following git command after you have cloned the repo.

```git checkout 2be4696e0072359fd98c14cd390526c0ed6ab90e```

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

