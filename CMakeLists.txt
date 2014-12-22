cmake_minimum_required(VERSION 2.8.9)

project(Slicer-Wasp)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://github.com/Tomnl/Slicer-Wasp")
set(EXTENSION_CATEGORY "Segmentation")
set(EXTENSION_CONTRIBUTORS "Thomas Lawson (MRC Harwell, Oxfordshire)")
set(EXTENSION_DESCRIPTION "A module to perform a series of ITK watershed segmentation (without seeds) and then let the user create a label map out of selected components.

An isosurface model will also be generated.
")
set(EXTENSION_ICONURL "http://www.slicer.org/slicerWiki/images/5/5b/Slicer-Wasp.png")
set(EXTENSION_SCREENSHOTURLS "http://wiki.slicer.org/slicerWiki/index.php/Documentation/Nightly/Extensions/Wasp")

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(Wasp)
## NEXT_MODULE

#-----------------------------------------------------------------------------


include(${Slicer_EXTENSION_CPACK})


