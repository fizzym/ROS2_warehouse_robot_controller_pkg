# ROS2_warehouse_robot_controller_pkg

### Description
Controls the robot in the [ROS2_warehouse_robot_spawner_pkg](https://github.com/fizzym/ROS2_warehouse_robot_spawner_pkg)

### Requirements
Ubuntu 20.04, ROS2 Foxy, [ROS2_warehouse_robot_spawner_pkg](https://github.com/fizzym/ROS2_warehouse_robot_spawner_pkg)

### Instructions
To run clone in ros2_ws/src:
```
cd ~/ros2_ws/src
git clone https://github.com/fizzym/ROS2_warehouse_robot_controller_pkg
```
Build the package using colcon:
```
cd ~/ros2_ws/
colcon build --packages-select warehouse_robot_controller_pkg
```
Source the workspace and launch the spawner package:
```
source install/setup.bash
ros2 launch warehouse_robot_spawner_pkg gazebo_world.launch.py 
```
Open a new terminal, source the workspace and launch the controller package:
```
source install/setup.bash
ros2 launch warehouse_robot_controller_pkg controller_estimator.launch.py
```

### Reference
Implements Automatic Addison ["How to Simulate a Robot Using Gazebo and ROS 2"](https://automaticaddison.com/how-to-simulate-a-robot-using-gazebo-and-ros-2/).
