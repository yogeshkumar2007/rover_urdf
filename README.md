# Rover URDF

ROS 2 description package for a six-wheel rover. The package contains the rover URDF, STL meshes, and a launch file that starts the robot state publisher, joint state publisher, and RViz2.

## Package layout

- `src/ros3/urdf/rover_model.urdf` - main rover model
- `src/ros3/meshes/` - STL visual and collision meshes
- `src/ros3/launch/display.launch.py` - display launch file

## Requirements

- ROS 2 with `ament_cmake` and `colcon`
- `robot_state_publisher`
- `joint_state_publisher`
- `rviz2`

## Build

From the workspace root:

```bash
source /opt/ros/<ros2-distro>/setup.bash
colcon build --symlink-install --packages-select ros3
source install/setup.bash
```

## Display the rover

```bash
ros2 launch ros3 display.launch.py
```

The generated `build/`, `install/`, and `log/` directories are intentionally excluded from version control.