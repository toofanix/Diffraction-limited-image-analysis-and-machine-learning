# Diffraction-limited-image-analysis-and-machine-learning

This repository contains three jupyter notebooks.

1. Image analysis using bspline.
   In this notebook, I used wavelet filter (B-spline) to detect diffraction limited single spots from fluorescent images.
   
2. Estimation of centroid using 2D gaussian fitting and classification.
   Here I apply the approach developed in notebook 1 to analysis a stack tiff image. The code analysis all the frames, and selects candidate single spots. All the spots are then fit to a 2D gaussian function in order to obtain the amplitude, the sub-pixel location of the spot in x and y, the standard deviation of the spot in x and y, and the background. Based on the characteristics of diffraction limited single spot images, I perform classification of whether a spot would be good or bad for super-resolution image.
