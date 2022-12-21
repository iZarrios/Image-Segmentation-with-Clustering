# Image Segmentation with Clustering

This repository explores the suitability of clustering methods for the task of image segmentation on the BSR dataset.


## Problem Statement

We intend to perform image segmentation. Image segmentation means that we can group similar pixels together and give these grouped pixels the same label. 
The grouping problem is a clustering problem. We want to study the use of K-means on the Berkeley Segmentation Benchmark. 
Below we will show the needed steps to achieve this goal.


### 1. Download the Dataset and Understand the Format

We will use Berkeley Segmentation Benchmark. The data is available at the following link.

http://www.eecs.berkeley.edu/Research/Projects/CS/vision/grouping/BSR/BSR_bsds500.tgz. 

The dataset has 500 images. The test set is 200 images only. We will report our results on the first 50 images of the test set only.

### 2. Visualize the image and the ground truth segmentation 
We wrote our own function that reads an image and display an image with its associated ground truth segmentation(s).

### 3. Segmentation using K-means

Every image pixel is a feature vector of 3-dimension {R, G, B}. We used this feature representation to do the segmentation.
We changed the K of the K-means algorithm between {3,5,7,9,11} clusters. 

We implemented the Kmeans algorithm as well as compared it with the SKlearn Kmeans function.

We evaluated the result segmentation using F-measure, Conditional Entropy for image I with M available ground-truth 

### 4. Big Picture

We selected a set of five images and displayed their corresponding ground truth against our segmentation results using K-means at K=5.

We then implemented an Normalized-cut algorithm with a similarity matrix built using the 5-Nearest Neighbours graph at K=5, and compared our results
with both the Ground Truth segmentations and the Kmeans predictions.


### 5. Extra 

In the previous parts, we used the color features RGB. We did not encode the layout of the pixels. We want to modify that for K-means
clustering to encode the spatial layout of the pixels. We added two features to the RGB image: x and y positions.



### 6. Check our report! 
A report detailing our background research as well as our work exists in the repo!
