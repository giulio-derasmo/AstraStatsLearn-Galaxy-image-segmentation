# [AstraStatsLearn] Galaxy image segmentation

University project at the course of Statistical Learning concerning **image segmentation** and object detection of **satellite images** of galaxies using different technique involving typical methods as Random Forest and KMeans, and neural networks like U-Net and Mask RCNN.

## The data

The Dataset is composed of three images (25000x25000 pixels) in FIT format, which allow to preserve the intensity of large images when imported and saved. The first image < img.fits > is the raw satellite image, then we have the < rms.fits > which is the error of the image, and < true.fits > which is the true segmentation.
In order to train the various model we split the images in patches of 256x256 pixels increasing the number of sample for our training.

## Pre-Processing

We use different technique to pre-process the images.
1. normalize the image using normalize of < astropy.visualization > library;
2. enhance the contrasts using FITS Liberator 3;
3. add rms to the image.

<p float="left">
  <img src="/images/original_patch.jpg" width="250" />
  <img src="/images/software_patch.jpg" width="250" /> 
  <img src="/images/final_preprocess.jpg" width="250" /> 
</p>


# 
<p align="center">
    <img src="https://user-images.githubusercontent.com/50860347/147412786-183da6b0-990f-4016-9f2e-0719d8066f5b.png" style="width: 100%"/>
<p>
