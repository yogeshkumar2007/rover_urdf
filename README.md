# Rover URDF

ROS 2 description package for a six-wheel rover. The package contains the rover URDF, STL meshes, and a launch file that starts the robot state publisher, joint state publisher, and RViz2.

## Package layout

- `src/rover_model/urdf/rover_model.urdf` - main rover model
- `src/rover_model/meshes/` - STL visual and collision meshes
- `src/rover_model/launch/display.launch.py` - display launch file

## Requirements

- ROS 2 with `ament_cmake` and `colcon`
- `robot_state_publisher`
- `joint_state_publisher`
- `rviz2`

## Build

From the workspace root:

```bash
source /opt/ros/<ros2-distro>/setup.bash
colcon build --symlink-install --packages-select rover_model
source install/setup.bash
```

## Display the rover

```bash
ros2 launch rover_model display.launch.py
```

The generated `build/`, `install/`, and `log/` directories are intentionally excluded from version control.