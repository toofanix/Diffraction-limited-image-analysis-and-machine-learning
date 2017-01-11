# Diffraction-limited-image-analysis-and-machine-learning

This repository contains three jupyter notebooks.

1. "Image analysis using bspline.ipynb"

   In this notebook, I used wavelet filter (B-spline) to detect diffraction limited single spots from fluorescent images.
   
   
2. "Estimation of centroid using 2D gaussian fitting and classification.ipynb"

   Here I apply the approach developed in notebook 1 to analysis a stack tiff image. The code analysis all the frames, and selects candidate single spots. All the spots are then fit to a 2D Gaussian function in order to obtain the amplitude, the sub-pixel location of the spot in x and y, the standard deviation of the spot in x and y, and the background. Based on the characteristics of diffraction limited single spot images, I perform classification of whether a spot would be good or bad for super-resolution image.
   
   
3. "Spot Classification using Machine Learning.ipynb"

   In this notebook, the take the dataset created in the previous notebook. The dataset consists of the images of all the spots that were detected in a stacked tiff file, and their classification based on the parameters obtained from fit to 2D Gaussian. I used this information to train a classifier that can perform classification of the images into good and bad spots.
