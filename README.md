# Sensor Fusion For Self-Driving Car

<img src="https://github.com/awbrown90/SensorFusionHighway/blob/master/media/ObstacleDetectionFPS.gif" width="700" height="400" />

In the field of autonomous vehicles, sensor fusion plays a crucial role in enhancing our understanding of the surrounding environment. By combining data from multiple sensors, such as lidar and radar, we can obtain a more comprehensive view of the world. In this code, we track multiple cars on the road, estimating their positions and speeds. Sensor fusion enables us to make informed decisions and ensure the safety and efficiency of self-driving cars.

**Lidar** sensors provide high-resolution data by emitting laser signals that bounce off objects. By measuring the time it takes for the signals to return, we can determine the distance to objects. Additionally, the intensity of the returned signal provides information about the object. Lidar sensors emit laser rays at various angles, covering a 360-degree range. While lidar sensors offer accurate 3D models of the environment, they are currently expensive, with standard units costing over $60,000.

**Radar** data is typically very sparse and in a limited range, however it can directly tell us how fast an object is moving in a certain direction. This ability makes radars a very pratical sensor for doing things like cruise control where its important to know how fast the car infront of you is traveling. Radar sensors are also very affordable and common now of days in newer cars.

**Sensor Fusion** by combing lidar's high resoultion imaging with radar's ability to measure velocity of objects we can get a better understanding of the sorrounding environment than we could using one of the sensors alone.

## Installation

### Linux Ubuntu 16

Install PCL, C++

The link here is very helpful, 
https://larrylisky.com/2014/03/03/installing-pcl-on-ubuntu/

A few updates to the instructions above were needed.

* libvtk needed to be updated to libvtk6-dev instead of (libvtk5-dev). The linker was having trouble locating libvtk5-dev while building, but this might not be a problem for everyone.

* BUILD_visualization needed to be manually turned on, this link shows you how to do that,
http://www.pointclouds.org/documentation/tutorials/building_pcl.php

