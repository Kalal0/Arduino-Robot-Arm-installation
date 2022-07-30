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

    1 - cd catkin_ws/src/
    2 - sudo apt install git
    3 - git clone https://github.com/smart-methods/arduino_robot_arm
