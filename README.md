# Palm_tracker_storm32_GC
This repo presents the code for a open palm tracking using a STorm32-BGC 3 axis gimbal controller hardware and a logitech c270 camera. Following task has been presented:

1. PID controller tuning of gimbal controller for better attitude tracking.
2. Object tracking (open palm of a person) using ros_deep_learning package (https://github.com/dusty-nv/ros_deep_learning).
3. Tracking the detected object at image center by passing orientation command to gimbal controller and move the camera.

### 1. PID controller tuning
Updating soon.

### 2. Object (open palm) detection
For detection, MobileNetV1-SSD model has been trained on open palm dataset collected in the laboratory. Few images are shown below.

![open_palm_detection](https://user-images.githubusercontent.com/37348142/198530061-75015330-25e7-4d8d-86b7-e0287eca5a46.jpg)

The deviation of detected palm from image center is calculated, corresponding angle (Yaw, Roll and Pitch) required to keep the detected object at image   center is calculated and communicated to gimbal controller.
#### Note: more data will be updated soon

### 3. Attitute command to hardware
ROS package for gimbal controller has been taken from McGill robotics (https://github.com/rk800506/stm32_bgc_ranjeet_version). Attitute commands can be communicated to the hardware.
#### Note: More data will be udpated soon.
