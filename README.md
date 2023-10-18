# Ice Nine Unitree

This is the ROS melodic package that integrates Unitree GO1 with EMLID Reach RTK GPS system.

## Dependencies
1. ROS melodic
2. [unitree_ros_to_real](https://github.com/ICE9-Robotics/unitree_ros_to_real/tree/unitree_go1) (our fork)
3. [robot_localisation](http://wiki.ros.org/robot_localization)
4. [emlid_reach_ros](https://github.com/tmxkn1/emlid_reach_ros)
5. [rtkgps_odom_matcher](https://github.com/tmxkn1/rtkgps_odom_matcher)

## Installation
The package needs to be installed on the Head Nano PC (192.168.123.15). See [Access the Unitree PCs](https://github.com/ICE9-Robotics/ice9_unitree/wiki/Access-the-Unitree-PCs) for connection instructions.

Once logged in the Head Nano PC, download all the packages:

```
git clone https://github.com/ICE9-Robotics/ice9_unitree.git ~/ice9_ws/src/ice9_unitree
git clone -b v3.8.0 https://github.com/unitreerobotics/unitree_legged_sdk.git ~/ice9_ws/src/unitree_legged_sdk
git clone https://github.com/ICE9-Robotics/unitree_ros_to_real.git ~/ice9_ws/src/unitree_ros_to_real
git clone -b melodic-devel https://github.com/cra-ros-pkg/robot_localization.git ~/ice9_ws/src/robot_localisation
git clone https://github.com/tmxkn1/emlid_reach_ros.git ~/ice9_ws/src/emlid_reach_ros
git clone https://github.com/tmxkn1/rtkgps_odom_matcher.git ~/ice9_ws/src/rtkgps_odom_matcher
```
Install dependencies:
```
git clone -b master https://github.com/ros-drivers/nmea_msgs.git ~/ice9_ws/src/nmea_msgs
cd ~/ice9_ws
rosdep install --from-paths src -i -y
```
Then build the package with `catkin_make`:
```
cd ice9_ws
caktin_make
```

## Use
```
roslaunch ice9_unitree unitree.launch
```
