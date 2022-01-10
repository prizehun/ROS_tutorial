# ROS_tutorial
ROS2 cicular moving turtle

## Package Create
```
cd ~/turtle_ws/src
ros2 pkg create rvd_action_interfaces --build-type ament_cmake
ros2 pkg create moving_turtle --build-type ament_python
```

## Build
in your work space
```
cd ~/turtle_ws
colcon build --symlink-install --packages-select rvd_action_interfaces
colcon build --symlink-install --packages-select moving_turtle
. ~/turtle_ws/install/local_setup.bash
```
## Launch
```
ros2 launch moving_turtle circularturtle.launch.py
```
## Topic publish
open other terminal
```
ros2 topic pub --once /rad_vel_dir rvd_action_interfaces/msg/RVD "{radius: 4.0, velocity: 10.0, direction: True}"
```
if direction is true(1) then turtle moves in counter clockwise direction.
else moves in clockwise direction

# ROS_example_1
ROS2 dwa ai moving turtle
