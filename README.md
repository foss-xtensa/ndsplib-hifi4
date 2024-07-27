# HiFi4_NDSP
NatureDSP Library for HiFi4 DSP cores

# The repo is organized as follows.

## xws:
  * Last stable release version of the NDSP containing two xws files.
  * An xws each, for the library-kernels and the test-driver.
    Ex : HiFi4_VFPU_v500_demo.xws & HiFi4_VFPU_v500_library.xws
  * Building and executing the xws in Xtensa Xplorer is described in the API Reference Document. 
  * Building and executing the source code in linux is described in the https://github.com/foss-xtensa/ndsplib-hifi4/tree/main/doc.
  * Detailed release documentation can be extracted from lib.xws/doc folder.

### Release v5.0.0 Brief: 
* Release Date : Jul 2024
* New APIs have been added to support Matlab Code Replacement Library. 
* Verification & testing has been done with a very limited number of LX8.0.3 HiFi-4 cores, using the RJ-2024.3 tool chain.
* Sanity testing has been done for backward compatibility on LX7.1.10 cores using RI-2023.11 tool chain .   

## NDSP_HiFi4
This contains the source code along with make files that will build in linux environment.  

## doc folder
This contains help documentation on how to build the source code in linux and run the performance and functional regressions. 
