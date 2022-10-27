CLASS_DMDR: Cosmic Linear Anisotropy Solving System for the Dark Matter-> Dark Radiation Model
==============================================

Authors: Colin Hill and Fiona McCarthy (jcolin.hill@gmail.com and fiona.mccarthy0@gmail.com)

This is a fork of the Einstein-Boltzmann solver CLASS v3 (https://lesgourg.github.io/class_public/class.html), written by 
Julien Lesgourgues, Thomas Tram, Nils Schoeneberg, et al.; refer to the original repository
for the README of CLASS.

All modifications to the original CLASS code are marked with a comment in the code containing 'DMDR modification'.


The DM-DR model
-----------------------------------

This model is a generalization of the decaying cold dark matter (DCDM) model already implemented 
in CLASS.  The scenario was first introduced in Bringmann et al. (2018): https://arxiv.org/abs/1803.03644.
We discussed it in detail in https://arxiv.org/abs/2210.14339

Compiling CLASS_DMDR and getting started
-----------------------------------

To install the C code, clone this repository from the terminal and then do:

    cd class_DMDR
    make clean
    make class

To avoid conflicts with other builds of CLASS, it is recommended you do the above in a new 
virtual environment. Note that you will need to have gsl installed and in your PATH.

To check that the code runs, do:

    ./class explanatory_DMDR.ini
    
If it runs with no error message, you have succeeded in installing the C code.
    
To install the C code along with the python wrapper, do:

    cd class_DMDR
    make clean
    make 
    
You will need to have numpy and cython installed (along with gsl, as before); to run
the python code, you will also need scipy.


Currently the Makefile is set to run without openmp ; if you wish to run the code in 
parallell, you can uncomment the relevant sections of the Makefile to run with openmp
but you will need an appropriate gcc compiler (i.e., not Clang).

Usage
-----------------------------------

To run the C code, you need a .ini file like explanatory_DMDR.ini ; you can
copy and edit this directly, and modify the parameters f_dcdm, a_t_dcdm, 
and kappa_dcdm. 

The code can also be run through the python wrapper; an example usage is in
the notebook notebooks/DMDR_example.ipynb .

If you use this code in a publication, please cite the paper https://arxiv.org/abs/2210.14339 .

Support
-----------------------------------

If you are having issues with the above, please feel free to email me at fiona.mccarthy0@gmail.com

Acknowledgments
-----------------------------------

This code has been checked by comparison to the modification to CAMB by Angela Chen:
https://bitbucket.org/anqich/ddm-camb/src/master/

We thank Angela Chen for making this public and for correspondence
about the code.
