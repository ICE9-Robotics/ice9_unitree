# Ice Nine Unitree

This is the ROS melodic package that integrates Unitree GO1 with EMLID Reach RTK GPS system.

## Dependencies
1. ROS melodic
2. [emlid_reach_ros](https://github.com/tmxkn1/emlid_reach_ros)
3. [robot_localisation](http://wiki.ros.org/robot_localization)
4. rtkgps_odom_matcher(https://github.com/tmxkn1/rtkgps_odom_matcher)

## Installation
The package needs to be installed on the Head Nano PC (192.168.123.15). See [Access the Unitree PCs](https://github.com/ICE9-Robotics/ice9_unitree/wiki/Access-the-Unitree-PCs)

## Use
```
roslaunch ice9_unitree unitree.launch
```
