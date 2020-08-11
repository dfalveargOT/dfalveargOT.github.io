---
layout: post
title: CropCount
date: 2020-01-09 00:00:00 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: CropCount.jpg # Add image post (optional)
fig-caption: # Add figcaption (optional)
feature: assets/img/CropCount.jpg
tags: [DeepLearning, Software, Open-Source, OpenCV] # add tag
comments: true
---

Deep learning approach to detect and count certain type of plants using geo-reference images taken by drones.

Technology have been impacting all industrial sectors such as, massive objects production, healthcare, agriculture, aeronautics and others, in the same way, there are a lot of business that keep their work based on hand made methods, the main key of the current situation is that, the technology could improve performance, product quality, and live quality. The budget invested in tech-education, as well as, they start to generate innovation make possible to companies to do big steps and establish good bases for the competitive future.

The CropCount project was develop with the objetive of automatizing human hand tasks, in this case, counting elements on images taken by drones, the need apart of being a tedious work, it generates health issues on hands and eyes for being a repetitive task, under those circumstances, the solution was satisfied improving time and reducing health and hand problems in employers, the software could count the same quantity of a human being in less time, and also generate a CSV containing the coordinates of each element detected. Let see a brief introduction of the project.

### The Research

TThe research had two approaches, the first version was consist of many traditional open-source tools, and the second version was developed for improving the accuracy of the design using deep learning.


#### Version 1.0
This version was designed using traditional computer vision tools like: OpenCV, Skimage, numpy and others. At the beginning, the image has to be load as .jpg or .png format, then the software use some color spaces and Fourier transform for extract important information of the crops, thus, the objetive is highlight the characteristics that compound a plant, this step is defined as preprocessing step, in the same way, the information are filtered by some morphological operation and segmentation tools, later the results are passed to a new step where the design find contours and the plants are detected with blob detector, at this point it already recognized and segmented the elements, but there are information that is duplicated and correspond to the same element, as a consequence, a new filter step was designed to increase the overall performance, finally, the software use some space filter conditions and integrates all the counts given by the layers, then, the information of plant pixel coordinates is given as a plain text.

![Cropcount]({{site.baseurl}}/assets/img/cropcount/CropCountV1.0.png)

There is widely known that the light and camera resolution are the variables that affects directly the efficient of a visual recognition system, under these circumstances, the idea of developing a second version was offered to solve this issues with the use of modern tools like deep learning.

All the implementation is available at [CropCount V1.0 repository](https://github.com/dfalveargOT/CropCount_V1.0.git).

![Cropcount]({{site.baseurl}}/assets/img/cropcount/cp15lateral.jpg)

#### Version 2.0

Version 2.0 is an inherit part of the structure of the first version, also tools and operative process, with the use of Tensoflow and Keras the software solve the major issues, firstly, the first design step was take images of crops with drones and extract almost 100.000 images of the plant to start the design a quick model to recognize the element, at the same time, the design added GPU computing power, supervised manipulation and georeference data.

![Cropcount]({{site.baseurl}}/assets/img/cropcount/CropCountV2.0.png)

The workflow of the solution start with GUI tools built on OpenCV for extract regions of the images and get the resolution of the plant creating an anchor box, this approach is combined with sliding window for evaluation the complete image, furthermore, the image is quantized in small parts given by the anchor box, and it is resized as a 1 dimension vector, all the data are computed by a neural network classifier on an Nvidia GPU GTX-2080, later on, it is used some score filters and non-max suppression to find where the plants are in the image, after all, the results are exported as a UTM coordinates for each element recognized, and a text report with useful information about the whole process.

### Results

The evaluation and validation of the complete software had been done in several images from different locations and time, in fact, it gives a good behavior without the inference of light and cloud density variation, the overall performance is about 90% of accuracy, some issues had been found due to drone altitude photo shoot and plant size, this will be an improvement to reduce human post-processing, eventually, the application is operative and the goal was completed reducing time from many days to some hours, lastly, some images are shown below about the process from the user GUI interaction to the final image mark count.


![Cropcount]({{site.baseurl}}/assets/img/cropcount/CropCountP3.png)
![Cropcount]({{site.baseurl}}/assets/img/cropcount/cp23.jpg)

Copyright © 2019 DataRock S.A.S. All rights reserved.

