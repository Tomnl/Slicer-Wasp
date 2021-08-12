Important for installation!
----------
Please use 3D Slicer version 4.5.0-1 - The 3D slicer installer for mac/windows or linux can be downloaded here https://slicer-packages.kitware.com/#collection/5f4474d0e1d8c75dfc70547e/folder/60add372ae4540bf6a89bea4

And then install WASP from the extension manager.

[WASP](http://wiki.slicer.org/slicerWiki/index.php/Documentation/4.4/Extensions/Wasp)
====



Watershed Annotation and Segmentation Plugin for 3D Slicer. For documentation see [Wiki ](http://wiki.slicer.org/slicerWiki/index.php/Documentation/4.4/Extensions/Wasp) and [Youtube] (https://www.youtube.com/watch?v=o9DA4gqWNjg&feature=youtu.be). Installation can be performed with the 3D Slicer [Extension manager](https://www.slicer.org/slicerWiki/index.php/Documentation/4.5/SlicerApplication/ExtensionsManager).


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

Other working versions
----
If you are using the 3D slicer 4.4 stable version the current version of WASP will not work. You will have to use the following git command after you have cloned the repo and install the plugin manually (without the extension manager).

```git checkout 2be4696e0072359fd98c14cd390526c0ed6ab90e```




