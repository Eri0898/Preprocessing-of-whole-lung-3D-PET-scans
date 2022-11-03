# Preprocessing-of-whole-lung-3D-PET-scans

This repository contains some preprocessing steps that can be applied on radiological scans using Python. Particularly, those steps have been written to work with PET scans, but they can also be applied on other radiological scans, such ad CT scans. 

In the following a brief description of all the steps is reported.
- The [first step](https://github.com/Eri0898/Preprocessing-of-whole-lung-3D-PET-scans/blob/main/First-preprocessing-step_Numpy-conversion-and-resampling.ipynb) consists in a numpy conversion and resampling of the original scans. The scans used in this work are in DICOM format, thus they need to be converted in numpy format to be managed in python. Then, a 1-mm resampling has been performed to make slices within scans spatially homogenous.
- The 
