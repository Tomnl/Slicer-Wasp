cmake_minimum_required(VERSION 2.8.9)

project(Slicer-Wasp)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://github.com/Tomnl/Slicer-Wasp")
<<<<<<< HEAD
set(EXTENSION_CATEGORY "Segmentation")
set(EXTENSION_CONTRIBUTORS "Thomas Lawson (MRC Harwell, Oxfordshire)")
set(EXTENSION_DESCRIPTION "A module to perform a series of ITK watershed segmentation (without seeds) and then let the user create a label map out of selected components.

An isosurface model will also be generated.
")
set(EXTENSION_ICONURL "http://www.example.com/Slicer/Extensions/Slicer-Wasp.png")
=======
set(EXTENSION_CATEGORY "Examples")
set(EXTENSION_CONTRIBUTORS "John Doe (AnyWare Corp.)")
set(EXTENSION_DESCRIPTION "This is an example of a simple extension")
set(EXTENSION_ICONURL "https://raw.github.com/Tomnl/Slicer-Wasp/master/Slicer-Wasp.png")
>>>>>>> c48e4ccebe2ca17159b088df8495565cc209a7ed
set(EXTENSION_SCREENSHOTURLS "http://www.example.com/Slicer/Extensions/Slicer-Wasp/Screenshots/1.png")

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(Wasp)
## NEXT_MODULE

#-----------------------------------------------------------------------------
<<<<<<< HEAD

include(${Slicer_EXTENSION_CPACK})

=======
include(${Slicer_EXTENSION_CPACK})
>>>>>>> c48e4ccebe2ca17159b088df8495565cc209a7ed
