---
layout: post
title: Agriculture automation
project: true
date: 2020-01-21 00:00:00 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: FlowersMachine.jpg # Add image post (optional)
feature: assets/img/FlowersMachine.jpg
tags: [Mechatronics, Computer Vision, Design, Software, Physics] # add tag
comments: true
---

How a simple industry need could be solved with technology to consequently improve human health and business performance.

The last few years, the develop of new technologies have been covering a widely industrial fields, however, in some latin america countries there is a delay in technifying companies, as a consequence, there are a lot of industries working with the same tech of the last decade. This post is an example how the human hand normally exposed to chemical elements for flowers could be improved reducing the exposure with the design and integration of computer vision, mechanical design, embed technology, sensors and physics.

![FlowersMachine]({{site.baseurl}}/assets/img/FlowersMachine/Definicion.2.jpg)

### The design process

As other research fields, the first point to attack was identify the main problem, in particular the leadership of the companies behind the develop, Color y Diseño S.A.S and Capiro S.A, give the insight about the process to be automatized, and the firsts brain storming meetings stablished a great team to start the design.

The need identified was improve the performance in the manufacture department of a specific product, and in the same way, reduce the effect of chemical elements to the employers. Given this  background, it was necessary to decide the main components needed for detailed tasks, the next image represent in most general form the engineering flowchart behind the machine, using embed devices for internet remote control, laser sensors, actuators, electro valves, pipes, conveyor belt system, and user interface for employer configuration.

![FlowersMachine]({{site.baseurl}}/assets/img/FlowersMachine/FlowersMachine.png)

### The Engineeting

The machine manage different technologies, firstly the user interface was develop with python, PyQt, and QT framework, this gave the possibility to integrate with small computers (Linux server embedded devices) to handle internet connection and control algorithms for image recognition (OpenCv, Sklearn) and movement system control, furthermore, the synchronization was develop analyzing the physics behind the flowers across the designed process, in addition, the digital components and the the power system like motors and AC-valves was done using Microchip 8 bits microcontrollers with an electronic PCB design containing pieces of analog circuits to handle noises, sensors, and communication protocols (SPI, UART) for linux communication.

![FlowersMachine]({{site.baseurl}}/assets/img/FlowersMachine/Electronics.jpg)


### Now Working

The human interaction with GUI interface gives the chance to control almost all the variables of the system, speeds, valves, and motors, subsequently the company could create specific programs to manage different type of products, giving a widely use of this automatization, in fact, after the human configuration the machine could handle in small periods of time bouquets of flowers, solving the need of improving manufacture performance, and on the other hand, the less people required to manage the machine reduce the exposure to chemical substances, as well as, all the quantities for the manufacture were standardized reducing the lost of this products. Lastly, the main brain of the machine is a watchdog that decides when and how to activate motors and valves in base of a recognition algorithm.

![FlowersMachine]({{site.baseurl}}/assets/img/FlowersMachine/Tracking.jpg)

### The Results

The prototype become to be a efficient industrial machine, some improvements were done, but the goal was achieved with great precision, the employers risks were diminished in big quantity, the manufacture time was improved for each operator, in the same way, the minimum sensor use and computer vision technology allows to reduce the maintenance and became important because the machine works fine for many conditions.


![FlowersMachine]({{site.baseurl}}/assets/img/FlowersMachine/Machine.jpg)

![FlowersMachine]({{site.baseurl}}/assets/img/FlowersMachine/Animation.gif)

Copyright © 2019 Color & Diseño S.A.S and Capiro S.A. All rights reserved.



