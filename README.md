# Visual-Servoing-Project

<h1 align="center"> Visual Servoing Project </h1> <br>
<h3 align="center"> Multi-Sensor Fusion & Tracking</h3> <br>
<p align="center">
University Of Burgundy
  <p align="center">
    <a href="https://www.vibot.org/"> <img src = "https://www.vibot.org/uploads/2/3/5/8/2358523/696297.png" width=60> </a>
  </p>
</p>
<h3 align="center">                       
Supervisor: 
</h3>
<p align='center'> Omar Tahri <p>
<h4 align="center">                       
Students:
</h4>
 <p align='center'>Nitinkumar ANAGHAN<a href="https://github.com/akhawaja2014"></a> <p> <br>
<h1 align="center">  </h1> <br>

## Introduction
This repository contains the requisite code for the visual servo related tasks to be implemented. The role is to allow a particular line to be followed by the robot. The challenges that I have experienced with the online platform are the reliability and the constraints of constructing a map that fits for our tasks. Fortunately, using the online platform, we were able to complete the line-follow mission.<br>

<h1 align="center">  </h1> <br>

## Implementation 
  - The Construct platform 

-Task 1 Follow Line

  - For the follow line task I used the construct platform to implement the task. The code is tested on different custom maps which are provided by the <a href="https://app.theconstructsim.com/#/Course/48"> OpenCV Basics for Robotics(Unit 5)</a>  and the <a href="https://app.theconstructsim.com/#/Course/5"> ROS Perception (unit 3) </a> courses in the construct platform. <br>

  - The Build platform courses have a static gazebo setting configuration where the robot and other model locations and orientations are difficult to monitor (Constraints in gazebo user interface setup where we will not be able to control the Robot using the Gzebo user interface), This is crucial because it is important for us to shift the robot quickly to various positions to verify that our algorithm works and that the robot can identify and follow the line from different positions.<br>

   -*To run the code:*
    I built a package named follow line task1 in the catkin ws workspace under the src name. This package is responsible for the role of following the line. - The follow line task.py file was generated in the followline package within the src folder. - The following package can be downloaded and imported into your catkin ws workspace or you can go straight to the construction portal (Perception course) and validate the code on the same map and then apply the followline package in their catkin ws workspace to the src folder. After that, by modifying the path to the catkin ws directory, you need to create the workspace and execute the catkin make command. - Type the roscd follow line task1/src/command in the terminal after the construction is finished. Now type python follow line task.py, and after the line, the robot should start.

