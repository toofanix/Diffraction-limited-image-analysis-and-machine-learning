# Diffraction-limited-image-analysis-and-machine-learning

This repository contains three jupyter notebooks.

1. "Image analysis using bspline.ipynb"

   In this notebook, I used wavelet filter (B-spline) to detect diffraction limited single spots from fluorescent images.
   
   
   
2. "Estimation of centroid using 2D gaussian fitting and classification.ipynb"

   Here I apply the approach developed in notebook 1 to analysis a stack tiff image. The code analysis all the frames, and selects candidate single spots. All the spots are then fit to a 2D Gaussian function in order to obtain the amplitude, the sub-pixel location of the spot in x and y, the standard deviation of the spot in x and y, and the background. Based on the characteristics of diffraction limited single spot images, I perform classification of whether a spot would be good or bad for super-resolution image.
   
   
   
3. "Spot Classification using Machine Learning.ipynb"

   In this notebook, the take the dataset created in the previous notebook. The dataset consists of the images of all the spots that were detected in a stacked tiff file, and their classification based on the parameters obtained from fit to 2D Gaussian. I used this information to train a classifier that can perform classification of the images into good and bad spots.
   

4. " Estimation of centroid using Machine Learning.ipynb"

   In these notebook, I take the dataset from the previous notebooks where I had performed a classification whether a spot image qualified for further analysis or not. Here, I take the qualified spots and try to estimate their sub-pixel centroid location using machine learning. I mainly use ridge regression in scikit learn, and linear regression in tensorflow to compare their results. In both cases, I am able to estimate the sub-pixel location of the centroid close to what would be obtained by 2D Gaussian fitting (std dev ~0.13 pixel). 
   The main advantage is that within machine learning, the centroids of many spots can be estimated in real time (as data is being collected) rather than post processing the data.
