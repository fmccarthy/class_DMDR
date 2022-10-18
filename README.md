CLASS_DMDR: Cosmic Linear Anisotropy Solving System for the Dark Matter-> Dark Radiation Model
==============================================

Authors: Colin Hill and Fiona McCarthy

This is a fork of CLASS (https://lesgourg.github.io/class_public/class.html) by 
Julien Lesgourgues, Thomas Tram, Nils Schoeneberg; refer to the original repository
for the README of CLASS


The DM-DR model
-----------------------------------

This model is a generalization of the decaying cold dark matter (DCDM) already implemented 
in CLASS.
It was introduced in https://arxiv.org/abs/1803.03644. 

Compiling CLASS_DMDR and getting started
-----------------------------------

To install the C code, clone this repository from the terminal and then do:

    cd class_DMDR
    make clean
    make class

To avoid conflicts with other builds of CLASS, it is recommended you do the above in a new 
virtual environment. Note that you will need to have gsl installed and in your PATH.

You might need to change your openmp flag in the Makefile, if you get an error, eg from 
-fopenmp to -openmp.



To check that the code runs, do:

    ./class explanatory_DMDR.ini
    
If it runs with no error message, you have succeeded in installing the C code.
    
To install the C code along with the python wrapper, do:

    cd class_DMDR
    make clean
    make 
    
You will need to have numpy and cython installed (along with gsl, as before); to run
the python code, you will also need scipy.

Support
-----------------------------------

If you are having issues with the above, please feel free to email me at fiona.mccarthy0@gmail.com
