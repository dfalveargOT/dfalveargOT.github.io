---
layout: post
title: Flowers Machine
project: true
date: 2020-01-21 00:00:00 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: FlowersMachine.jpg # Add image post (optional)
feature: assets/img/FlowersMachine.jpg
tags: [Mechatronics, Computer Vision, Design, Software] # add tag
comments: true
---

The inference of the new technological fields in the industry has been covering the world with great improvements in many fields, this post talk about the inference of mechatronics, physics, computer vision, and design, for to automatize hand made manufacture process in flower’s companies, this work was in collaboration with Color & Diseño S.A.S and Capiro S.A.

Colombia invest in the flower industry for the excellent weather conditions across the year, research in new products as well as the improvement in time and cost give competition opportunities worldwide and allow the growth of Colombia in the world commerce. This machine was the result of looking to get better results in processing flowers for local and world sales, reducing risk in employers that use chemical elements that could generate future health problems. 

![FlowersMachine]({{site.baseurl}}/assets/img/FlowersMachine/Definicion.2.jpg)

### The research

The research process took 10 months from problem understanding to functional prototype operation, the initial design placed above represents the most general approach of the final idea, all the design was done with real dimensions ready for implement. There were many brainstorming meetings to generate the ideas and take it to the real world, doing experiments with real flowers looking to implement motors, software, electronics, and sensors to achieve the main goal proposed by the company. The team that worked on the project was interdisciplinary, from technical skills people to engineers from company industrial operations to development engineers. I recall the importance of each person without thinking in graduate tittles, great ideas came from very creative people without any bachelor o tech studies.

![FlowersMachine]({{site.baseurl}}/assets/img/FlowersMachine/FlowersMachine.png)

The brain of the machine receives bouquets of flowers and makes the physics process on it,  enhancing beauty characteristics and giving non-natural secret aspects. This system is designed in four principal modules, first, the operator configures the process to be done, times and raw material, then the bouquets start the process which computer vision algorithms recognize the object and track the movement where the main control will activate the motors and processing modules composed by actuators, valves, and pipes. The main goal achieved was the possibility to process multiple bouquets at the same time, so the improvement in time was about 20 times faster than manual human processing.

The image below shows the recognizing and tracking module, the employer configure in a main screen with GUI interface all the process for the current flower type, then other screen shows and control the computer vision algorithm while the main control algorithm receive the communications of the belt system as well as the intelligent vision system, we can see the flower passing over a camera and continuing to the procedures.


![FlowersMachine]({{site.baseurl}}/assets/img/FlowersMachine/Tracking.jpg)

### The Development
Looking back to the engineering, for each module combine a series of powerful tools, for the motor, actuators, and control we used C language program on Microchip technology, furthermore, it performs communication task with the main brain control, all the design was done in Eagle software and Colcircuitos was the company electronics manufacturer. For the user GUI operation, it was programmed in python, QT over Linux server embedded device, which performs communication and organization tasks, human-machine interaction, and deciding capabilities, this is the manager of all the machine, receives the decisions of the computer vision module composed by a camera and python algorithms to decide the future processing for bouquets of flowers. The under images show the process from prototype design to electronic PCB design and box control building.

![FlowersMachine]({{site.baseurl}}/assets/img/FlowersMachine/Electronics.jpg)

### The Results

The prototype becomes to be an efficient industrial machine, and some improvements were done, but the goal was achieved with great precision, the employers risks were diminished in big amount, the manufacture time improves above 100% for each operator, the minimum sensor control and computer vision technology allows to reduce the maintenance and became important because the machine works for many conditions. Some images of the complete machine were presented, also the bouquets process and belt system transportation.


![FlowersMachine]({{site.baseurl}}/assets/img/FlowersMachine/Machine.jpg)

![FlowersMachine]({{site.baseurl}}/assets/img/FlowersMachine/Animation.gif)

Copyright © 2019 Color & Diseño S.A.S and Capiro S.A. All rights reserved.



