# Single Robot Mapping and Navigation with the ROS-Navigation-Stack (Only test on ubuntu 20.04 - ROS Noetic)

## Required dependencies
    sudo apt install ros-noetic-gmapping
    sudo apt install ros-noetic-map-server
    sudo apt install ros-noetic-navigation
## Donwload and compile the project
    cd catkin_ws/src/
    git clone https://github.com/Shuteng-0608/single_nav.git
    cd ..
    catkin_make -DCATKIN_WHITELIST_PACKAGES="single_nav"
## Mapping the Gazebo world (SLAM - GMapping)
Mapping with keyboard
    roslaunch urdf02_
