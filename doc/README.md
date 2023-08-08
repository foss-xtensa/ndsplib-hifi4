# How to Build and Run the Source Code in Linux environment
  * Get the latest or required version of NDSP HiFi4 Code from GitHub archived in zip format.  
  * https://github.com/foss-xtensa/ndsplib-hifi4/tree/main/NDSP_HiFi4
  * Unzip or extract to the destination directory. 

## The source code is organized as follows.
  * **build** - contains the make file 
  * **library** - contains the optimized kernel functions for the HiFi core 
  * **testdriver** - contains the demo driver code to tun the library   

### It is assumed that the required HiFi core configurations and the Xtensa toolchain are installed in the Linux environment.
 An example .cshrc file that sets up the build environment accordingly is provided for reference 

## Setting up the environment 
  * A typical way is to place this .cshrc file in your home directory and execute the following from the command line terminal... 
  * source ~/.cshrc 
  * ri8
  * setenv XTENSA_CORE CORE_NAME     
    Ex: setenv XTENSA_CORE AE_HiFi4_LE5_AO_FP  

## Compiling the Source Code: 
  * Navigate to the testdriver directory:   …/ NDSP_HiFi4/build/project/xtclang/testdriver
  * **CLEAN:**  make clean -j -e LANG=LLVM  
  * **BUILD:**  make all -j -e LANG=LLVM 


## Running the executable: 
  ### Navigate to the bin directory: …/ NDSP_HiFi4/build/bin
  ### Performance tests:     
  * xt-run testdriver-AE_HiFi4_LE5_AO_FP_llvm-Xtensa-release -mips -brief 
  * xt-run testdriver-AE_HiFi4_LE5_AO_FP_llvm-Xtensa-release -mips -full   
  ###	Functional tests:
  * xt-run --turbo testdriver-AE_HiFi4_LE5_AO_FP_llvm-Xtensa-release -func -brief
  * xt-run --turbo testdriver-AE_HiFi4_LE5_AO_FP_llvm-Xtensa-release -func -full
  * xt-run --turbo testdriver-AE_HiFi4_LE5_AO_FP_llvm-Xtensa-release -func -brief -verbose 
  * xt-run --turbo testdriver-AE_HiFi4_LE5_AO_FP_llvm-Xtensa-release -func -full -fir -verbose 
  * xt-run --turbo testdriver-AE_HiFi4_LE5_AO_FP_llvm-Xtensa-release -func -brief -fir -iir -fft
