cmake_minimum_required(VERSION 3.1)
project(ice9_unitree)

find_package(catkin REQUIRED)

catkin_package()

install(DIRECTORY launch/
    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
)

install(DIRECTORY params/
    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/params
)
