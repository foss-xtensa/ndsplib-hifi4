# HiFi_4_NDSP
NatureDSP Library for HiFi 4 DSP cores

# The repo is organized as follows.

## xws:
  * Last stable release version of the NDSP containing two xws files.

  * An xws each, for the library-kernels and the test-driver.
    Ex : HiFi4_VFPU_Demo_v4_1_1.xws & HiFi4_VFPU_Library_v4_1_1.xws.xws

  * Building and executing the xws in Xtensa Xplorer is described in the API Reference Document. 
  * Detailed release documentation can be extracted from lib.xws/doc folder.

### Release v4.1.1 Brief: 
  * Release Date : February 2022.  
  * This release is targeted for xt-clang compiler, using RI2021.8 toolchain version.

## NDSP_HiFi4
This contains the source code along with make files that will build in linux environment.  

## doc folder
This contains help documentation on how to build the source code in linux and run the performance and functional regressions. 
