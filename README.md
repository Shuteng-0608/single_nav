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
    source ./devel/setup.bash
## Mapping the Gazebo world (SLAM - GMapping)
In **Terminal 01** 

    cd catkin_ws/
    source ./devel/setup.bash
    roslaunch urdf02_gazebo demo03_env.launch
In **Terminal 02**

    cd catkin_ws/
    source ./devel/setup.bash
    roslaunch nav_demo nav01_slam.launch
In **Terminal 03**

    cd catkin_ws/
    source ./devel/setup.bash
    rosrun teleop_twist_keyboard teleop_twist_keyboard.py

In **Terminal 04**

    cd catkin_ws/
    source ./devel/setup.bash
    roslaunch nav_demo nav02_map_save.launch
