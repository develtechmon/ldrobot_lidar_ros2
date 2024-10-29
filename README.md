# Getting Started

This is userguide on how i establish a fix frame in `ld06` lidar which later used for SLAM and localization.
This package is based on `ldrobot-lidar-ros2`.

This is an extension userguide from this guide
```
https://github.com/develtechmon/ROS2/blob/main/UserGuide/ros2_humble_nav2_and_SLAM_Setup.md
```

What i did here, i separate the `ldlidar_with_mgr_tech.launch.py` with `slam` command. You can follow,
this userguide on how i set this separation and how i launch the `lldiar_with_mgr_tech.launh.py` using command
line and `slam  script`.

## Step 1 : 


Open new terminal in your PC and run Command Line To launch Slam Tool Box. Here, we remap `/scan` topic to `/scan:=/ldlidar_node/scan` topic.
```
ros2 run slam_toolbox async_slam_toolbox_node --ros-args --params-file src/ldrobot-lidar-ros2/ldlidar_node/params/slam_toolbox.yaml --remap /scan:=/ldlidar_node/scan
```
