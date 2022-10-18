CLASS_DMDR: Cosmic Linear Anisotropy Solving System for the Dark Matter-> Dark Radiation Model
==============================================

Authors: Colin Hill and Fiona McCarthy

This is a fork of CLASS (https://lesgourg.github.io/class_public/class.html) by 
Julien Lesgourgues, Thomas Tram, Nils Schoeneberg; refer to the original repository
for the README of CLASS


Compiling CLASS_DMDR and getting started
-----------------------------------

Clone this repository from the terminal and then do:

    cd class_DMDR
    make clean
    make class

To avoid conflicts with other builds of CLASS, it is recommended you do the above in a new 
virtual environment.

To check that the code runs, type:

    ./class explanatory_DMDR.ini

The DM-DR model
-----------------------------------

This model is a generalization of the decaying cold dark matter (DCDM) already implemented in CLASS.
It was introduced in https://arxiv.org/abs/1803.03644. 
