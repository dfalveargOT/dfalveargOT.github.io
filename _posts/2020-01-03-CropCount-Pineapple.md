---
layout: post
title: CropCount Pineapple
date: 2020-01-09 00:00:00 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: CropCount.jpg # Add image post (optional)
fig-caption: # Add figcaption (optional)
feature: assets/img/CropCount.jpg
tags: [DeepLearning, Software, Open-Source, OpenCV] # add tag
comments: true
---
The importance of technology has been impacting all industrial sectors, such as massive objects production, healthcare, agriculture, and others, giving the prospect of growth due to the huge hand made methods that exist in the industry, furthermore the budget inverted in tech-education as well as they invest in innovation make possible to companies to do big steps and stablish good bases for the competitive future.

### The Why
The CropCount project become in production on early of 2019 at Datarock S.A.S offices,  on a speech about innovation and process improvement, the big challenge proposed is to create a software to support the engineering team for replacing the manual count of pineapple crops, in that time many people were counting big image taken by drones each plant of this fruit, and an exhausted feeling was present by the team for the tedious and monotonous work, the solution suggested gave them a better and a healthy way to do their job, the results of the project were satisfying improving time and reducing health hand problems in the employers, the same quantity that a person can count, the software do it with less time, for plant counting-recognizing takes around 50 milliseconds.

![Cropcount]({{site.baseurl}}/assets/img/cropcount/Cropcount-Process.png)

### The process

The research had two approaches, the first version was consist of many traditional open-source tools, and the second version was developed for solving some important issues on the performance of the first version.

#### Version 1.0
This version consists of traditional computer vision tools using OpenCV, Skimage, numpy and others. In the firsts instance the image has to be load as .jpg or .png format, then is used some color spaces and Fourier transform for show important information of the crops, resalting the characteristics that compound a plant, this step is defined as preprocessing step, suddenly the information is filtered by some morphological operation, and segmentation tools for later pass the data to match core process step, where tools like contours finding and blob detector detect the plants, next is used in filter step some vector coordinates modifications to eliminate duplicated counts and increase the overall performance, finally some space filter condiction as well as counting integration for all layers give the coordinates concerning each plant as well as an image drawing the overall process.

![Cropcount]({{site.baseurl}}/assets/img/cropcount/CropCountV1.0.png)

The issues that became important for the development of the second version was, the difficulty to maintain the performance of the software for light and resolution variation, the testing result in a great score for great image conditions (not always present for sun position, cloud density, and drone altitude), thus and idea of standardizing it became complicated, so the only way to reduce the effect of light, contrast, and resolution is using deep learning tools.

All the implementation is available at [CropCount V1.0 repository](https://github.com/dfalveargOT/CropCount_V1.0.git).

![Cropcount]({{site.baseurl}}/assets/img/cropcount/cp15lateral.jpg)

#### Version 2.0

The lot of software development information build with open-source tools give the chance for engineers to progress so fast, improving products and applications, the importance of share work with others creates a cooperative work sense allowing us to act collectively. All this development have been produced on Python, working with OpenCV, TensorFlow, numpy and other big tools to make possible really good industrial solutions as well as the growth capacity due the community support, I recall this to inspire and teach for others the value of continue working together and growing up the community.

Version 2.0 of this software inherit part of the structure of the last version, tools, and operative process, this develop fix the major problems with the use of deep learning tools based on TensorFlow and Keras, consequently was necessary to extract more than 100.000 images of pineapple plants taken by aerial vehicles, this value allows the training a neural network for a classifier operation, the complete process that an image takes for to count the crops is below, and some additional improvements were added like, georeference information, supervised manipulation, and fast computing.

![Cropcount]({{site.baseurl}}/assets/img/cropcount/CropCountV2.0.png)

The blocks that compound this solution starts with some GUI tools built-in OpenCV, allows for the user to extract regions of interest from the complete image, and also get the resolution of the plants for create an anchor box, this will allow to implement sliding window technic for evaluating the complete image in a series of grid points, furthermore is created vectors and batch of windows images with anchor box by the pixel resolution chosen by user, all this information is computed by a neural network classifier on an Nvidia GPU GTX-2080 improving time, finally, some scores filters and non-max suppression give the results of where the plants are in the image, the results are exported as a UTM coordinates for each plant recognized, and text report with useful information.


### Results

The evaluation and validation of the complete software have been done in a series of images for different crops locations and hours giving good behavior respect of light and cloud density, the overall performance is about 93% of effectiveness some issues have been encountered by the drone altitude photo shoot and pineapple plant diameter, this is an improvement that will be done to reduce human post-processing, eventually, the application is operative and the goal was completed reducing time from many days to some hours in count as well as human wear. Some images are present below of the process from the user GUI interaction to the final image mark count.

![Cropcount]({{site.baseurl}}/assets/img/cropcount/CropCountP3.png)
![Cropcount]({{site.baseurl}}/assets/img/cropcount/cp23.jpg)

Copyright © 2019 DataRock S.A.S. All rights reserved.

