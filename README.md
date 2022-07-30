# Arduino-Robot-Arm-installation
  These steps will cover the installation of the Arduino robot arm. This is assuming ROS has been successfully installed, if not please refer to this link: https://github.com/Kalal0/ROS-Installation-steps-for-PC-and-JetsonNano </br>
  
Ubuntu version: 20.04.4 </br>
ROS version: Noetic




## Creating a ROS Workspace: 

Input these commands in the cmd: 
    
    1 - source /opt/ros/noetic/setup.bash
    2 - mkdir -p ~/catkin_ws/src
    3 - cd ~/catkin_ws/ 
    4 - catkin_make
    5 - source devel/setup.bash
    
Now your ROS workspace is ready to have packages installed in it. 



## Installing Arduino Robot Arm Package: 

Part I

These commands will add the ardunino robot arm package to the src folder: 

    1 - cd catkin_ws/src/
    2 - sudo apt install git
    3 - git clone https://github.com/smart-methods/arduino_robot_arm
    
Part II

These commands will install all the necessary dependencies: 

    4 - cd catkin_ws
    5 - sudo apt-get install ros-noetic-moveit
    6 - sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
    7 - sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
    8 - sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control

Part III

This final command will compile all packages in your src folder: 

    9 - catkin_make
    
    
## Test your installation: 

Before attempting to run anything using ROS you must first set your source setup file (This must be done for each new shell instance). To do so, paste this line into your cmd: 

    source /home/myuser/catkin_ws/devel/setup.bash
    
"myuser" is switched out with your local username.

Open the robot arm in rviz by inputing: 

    roslaunch robot_arm_pkg check_motors.launch

![image](https://user-images.githubusercontent.com/109832303/181914380-b8ede4df-c41f-4395-aa87-aed635f04739.png)


You can also open the schematic in Moveit or Gazebo: 

Gazebo:

    roslaunch robot_arm_pkg check_motors_gazebo.launch

![image](https://user-images.githubusercontent.com/109832303/181914754-9262e54d-3b52-45ae-a550-2bc0a44ece03.png)

    
Moveit: 


    roslaunch moveit_pkg demo.launch
    
![image](https://user-images.githubusercontent.com/109832303/181914809-662e750c-0521-422c-b3eb-f3eda3b338f2.png)
 
 
 
If any of these three options open the schematic successfully, then your installation was correct and error free. You can now tweak and edit everything to your liking.

