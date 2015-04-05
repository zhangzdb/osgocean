## Change List ##

## osgOcean 1.0.1 ##

_Released: 03/11/09_

**Bug Fixes:**

  * Replaced references to depreciated textureRects in shaders
  * Removed implicit conversions from shaders
  * Depth of field getters/setters no longer cause a conflict on WIN32 platform
  * setDofFar now assigns the far variable rather than the near.
  * Extensionless headers are now placed in the headers folder within Visual Studio
  * CMake will no longer ask linux users to supply debug versions of dependancies in order to build
  * Search hints added to CMakelists for FFTSS
  * Changed <GL/gl.h> to <osg/GL> for mac compatability

**New Functionality:**

  * Removed all implicit conversion of ref\_ptr to ensure compatability with OSG v2.6
  * Added function to stop/start the ocean animation
  * Added support for adjustable reflection damping in FFT simulation
  * Improved effeciency of the FFT surface generation
  * Made OceanCylinder a part of osgOcean itself so it's always present with the ocean
  * Ocean height can now to be changed
  * Added interpolation functions to find the height and normal at any point on the ocean surface
  * Added a new case to the example to illustrate collision detection
  * Added flag to disable all shaders and use only fixed pipeline
  * Underwater Scattering can now be enabled/disabled
  * Reflection/Refraction passes can now automatically enabled/disabled based on height
  * Reflection/Refraction passes are only done if the water surface is visible
  * Reflection/Refraction passes are skipped if a shadow camera is detected