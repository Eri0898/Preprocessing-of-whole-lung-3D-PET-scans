# Preprocessing-of-whole-lung-3D-PET-scans

This repository contains some preprocessing steps implemented in Python that can be applied on radiological scans. Particularly, those steps have been written to work with PET scans, but they can also be applied on other radiological scans, such ad CT scans. 

In the following a brief description of all the steps is reported.
- The [first step](https://github.com/Eri0898/Preprocessing-of-whole-lung-3D-PET-scans/blob/main/First-preprocessing-step_Numpy-conversion-and-resampling.ipynb) consists in a numpy conversion and resampling of the original scans. The scans used in this work are in DICOM format, thus they need to be converted in numpy format to be managed in Python. Then, a 1-mm resampling has been performed to make slices within scans spatially homogenous.
- The [second step](https://github.com/Eri0898/Preprocessing-of-whole-lung-3D-PET-scans/blob/main/Second-preprocessing-step_Slice-selection-centering-the-lung-volume.ipynb) consists of slice selection centering the lung volume. This step is performed “manually”, meaning that the initial and final slices to be kept are selected one by one by observing the scans, as well as the black parts to be removed around the body volume. This step is essential to enormously reduce the dimension of each scan and to remove all the useless black pixels from the images.
- In the [third step](https://github.com/Eri0898/Preprocessing-of-whole-lung-3D-PET-scans/blob/main/Third-preprocessing-step_Normalization-and-enhancement.ipynb) an enhancement of the scans is performed by increasing the contrast, sharpening the images, and reducing the noise. Moreover, in this step all the images are being normalized so that, at the end, each pixel value lied between 0 and 1. The normalization has been simply implemented by subtracting each pixel by the minimum value of all the pixels and dividing by the range of values. 
- The [last step](https://github.com/Eri0898/Preprocessing-of-whole-lung-3D-PET-scans/blob/main/Last-step_Size-standardization.ipynb) is the one needed to standardize the dimensions of the scans. This step is needed, for example, when you need to use the scans to train a neural network; in this case it is essential to have all the scans with the same dimension. Specifically, in this script, the size chosen is 250x200x250 pixels. However, this dimensions can be changed according to your specific needs.

The following picture shows an example of the results that can be obtained with this preprocessing steps. Particularly, this reported is a PET scan. The one on the top is the original image, obtained after the first step. The image in the middle is the result after the second step. The last picture is the result after the third preprocessing step. 

<p align="center">
<img width="330" alt="Schermata 2022-11-03 alle 11 26 25" src="https://user-images.githubusercontent.com/111573018/199699836-1c60f78c-7b4a-4823-9fcc-e8df549a6b4d.png">
</p>
