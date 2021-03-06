---
title: Object classification with the Baxter robot
summary: This project shows the development of various classification tasks in static and dynamic environments with the Baxter robot based on color, using also a conveyor where pieces are transported to be classified in real time.

tags:
- Robotics
- Baxter
- Object classification
date: "2016-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

authors: 
- Francisco Barranco

image:
  caption: ""
  focal_point: Smart

links:
- icon: github
  icon_pack: fab
  name: Visit
  url: https://github.com/cristgl/TFG
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---

# Object classification tasks using the Baxter robot
This project shows the development of various classification tasks in static and dynamic environments with the Baxter robot. This robot will separate two groups of objects with different colours, positions and sizes, using the Robot Operating System (ROS Kinetic) on Ubuntu 16.04 LTS, MoveIt! and the OpenCV library for the computer vision, based on the colour filter made by [Maik Heufekes](https://github.com/cvr-lab/baxter_pick_and_place). Check the [Youtube videos](https://www.youtube.com/channel/UC9pq0ErS5dWzlCzpUrRdZlg/videos?view_as=subscriber).
 
# Prerequisites

   ## Workstation Setup

To set the workstation, the tutorial from [Rethink Robotics has been consulted](http://sdk.rethinkrobotics.com/wiki/Workstation_Setup), in this site you can find the installation of Ubuntu, the ROS specific version for that Ubuntu version, the Baxter SDK and the instructions for establishing the first comunication with the robot, which requires an Ethernet connection.

    Example: Network Connection->Add->Ethernet
    Connection name: Baxter
    IPv4 Settings: Method: Manual
    Address: 169.254.0.10, Netmask: 255.255.0.0, Gateway: 0.0.0.0
   
   ## MoveIt

   [MoveIt!](http://sdk.rethinkrobotics.com/wiki/MoveIt_Tutorial) is used for the motion planning, manipulation and collision checking.
   
   Moreover the package [moveit_python](https://github.com/mikeferguson/moveit_python) by Michael Ferguson needs to be installed.
   
   ## Robot arm calibration

   It is recommended to calibrate Baxter's arms for getting more precise results. [On the website](http://sdk.rethinkrobotics.com/wiki/Arm_Calibration) there are two different calibration routines which are very well described.
   
   ## Colour of the objects

   The object recognition can only work if the colours of the objects are known. The colours are defined in the baxter_img.cpp file as low and high HSV values. The best way to get the color values from an object which should be detected is to take pictures with the Baxter camera from it on the workspace in different positions and with different illuminations. 

    $ rosrun image_view image_view image:=/cameras/right_hand_camera/image

   This command opens a window with a stream of images from Baxter's right hand camera and allows to save images by right-clicking on the display window.
    Then the images can be analyzed with the [hsvThresholder.py file](https://github.com/saurabheights/IPExperimentTools/tree/master/AnalyzeHSV). Open a new terminal and execute the python file from the location where it is saved.

    $ python hsvThresholder.py frame0000.jpg

# Tasks Overview

There are two main classification tasks using a paddle and a wedge as tools, the first one is used in static classification and the other one in dynamic. Both of them are made out of cardboard and it is common that sometimes the objects weight more than the tools, resulting on difficulties at the time of classifying. The clustering algorithm used is K-means with k = 2, it separates the objects by colour and position. This algorithm gives us the centroids of both groups so that we can get the middle point.


## Static environment classification

Baxter classifies objects on the top of a table, setting them aside.

The project must be added in the src folder from the workspace and can be launched after it is built from a sourced terminal.

{{< youtube wTfLTKC_PFo >}}

Open a new terminal:

    $ source /opt/ros/kinetic/setup.bash
    $ source ros_ws/devel/setup.bash
    $ cd ros_ws/
    $ ./baxter.sh
    $ catkin_make
    $ roslaunch classif classification.launch

## Dynamic environment classification using a wedge

For making this classification, the speed of the objects on the conveyor belt has to be calculated. Then, the Baxter robot will predict where the objects are to separate them.

{{< youtube crF7NCy9WJw >}}

The project must be added in the src folder from the workspace and can be launched after it is built from a sourced terminal.
Open a new terminal:

    $ source /opt/ros/kinetic/setup.bash
    $ source ros_ws/devel/setup.bash
    $ cd ros_ws/
    $ ./baxter.sh
    $ catkin_make
    $ roslaunch dyn_wedge dyn_wedge.launch

## Dynamic environment classification using a paddle

For making this classification, the speed of the objects on the conveyor belt has to be calculated. Then, the Baxter robot will predict where the objects are to separate them. In this case, the tool used is a paddle, so it will be necessary to predict the position twice, as it can be seen in the video.

The project must be added in the src folder from the workspace and can be launched after it is built from a sourced terminal.

{{< youtube BypfZhM5Lto >}}

Open a new terminal:
    
    $ source /opt/ros/kinetic/setup.bash
    $ source ros_ws/devel/setup.bash
    $ cd ros_ws/
    $ ./baxter.sh
    $ catkin_make
    $ roslaunch dyn_classif dyn_classif.launch

# Packages

* **classif**. It includes the classification in a static environment.
* **dyn_classif**. Classification in a dynamic environment using a paddle.
* **dyn_wedge**. Classification in a dynamic environment using a wedge.
* **pick_and_place**. Adapted pick and place program for executing it in the Baxter robot.

The files included by this packages are:
* baxter_img.cpp: This C++ program identifies the objects in the image, visualizes them and calculates the middle point between the two groups of objects, sending them to the control file.
* file.py: It is the control file, it subscribes to the "clasificacion" or "detected_objects" topic and plans the trajectories and execute them to separate or pick the objects.
* file.launch: This launch file runs all the required nodes to accomplish the task.
