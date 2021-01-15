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
     - In [catkin_ws](https://github.com/MahBadran93/VisualServoingProject/tree/main/catkin_ws) workspace, under [src](https://github.com/MahBadran93/VisualServoingProject/tree/main/catkin_ws/src) folder we created a package called [followline](https://github.com/MahBadran93/VisualServoingProject/tree/main/catkin_ws/src/followline). This package is responsible for the line follow task. 
     - [follow_line.py](https://github.com/MahBadran93/VisualServoingProject/blob/main/catkin_ws/src/followline/src/follow_line.py) file has been created   inside the [src](https://github.com/MahBadran93/VisualServoingProject/tree/main/catkin_ws/src/followline/src) folder in the [followline](https://github.com/MahBadran93/VisualServoingProject/tree/main/catkin_ws/src/followline) package.
     - You can download the [followline](https://github.com/MahBadran93/VisualServoingProject/tree/main/catkin_ws/src/followline) package and import it into your **catkin_ws** workspace or you can go directly to the construct platform (Perception course unit 3) to test the code on the same map then add the **followline** package to **src** folder in their **catkin_ws** workspace. 
     - After that, you need to build the workspace by changing the path to **catkin_ws** directory and run the **catkin_make** command.
     - After the building is done, type **source/devel/setup.bash** command in the terminal.
     - Now, type **rosrun followline follow_line.py** and the robot should start following the line. 
     - Video demonstration below: 
       <p align="center">
        https://www.loom.com/share/e3fb418493244c50b8359afff7d42a46
       </p> 
     - As we discussed before, we tried to use **Ros Development Studio** in the construct platform to be able to easily change the Robot pose. To import the map (we choose to import the map provided by the OpenCv course unit 5) two packages needed, [opencv_course_sims](https://bitbucket.org/theconstructcore/opencv_course_sims/src/master/) and **rosbot_husarion** where they include the map files (models, world, urdf, launch). Click  <a href="https://app.theconstructsim.com/#/l/c8d160f/"> Here </a> to go to the project page in **ROS Development Studio** (you need to login to the construct platform).
     - After launching the project in **ROS Development Studio**, you can customize your screen layout and open the important applications like terminal, gazebo, Rviz graphic tool.
     - To run the code you need to import the map by typing **roslaunch unit_5_sim course_simulation_5.launch** in the terminal and wait till you see the map fully rendered in the gazebo application.
     - When you see the map fully rendered, you can control the Robot pose using gazebo but you need to be sure that the robot camera can see the line. You can check by using the **rqt** graphic tool, type **rqt_image_view** and you will see the camera view in Rviz.
     - After that, run the **follow_line.py** file. Type **rosrun followline follow_line.py**
     - video demonstration below: 
       <p align="center">
        https://www.loom.com/share/33ca77c452934220803740d948a3f46c
       </p>
     - Using the map from the opencv course and importing it in **ROS Development Studio** for the follow line task was good interm of the ability to customize our maps and add models and easily change their positions but the problem is the stability and the rendered map can sometimes be different from the map in the course where it leads to some performance issues. For example, sometimes it can be noticed that the rendered map is more dark and affect the quality of the images observed by the Robot which affect the algorithm performance.
    

