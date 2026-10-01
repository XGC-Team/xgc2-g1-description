# g1_description

Reusable **visual** ROS description assets for **Unitree G1** (`g1`).

Package layout follows `b2arx_description`: meshes + visual URDF only. No
controllers, Gazebo plugins, or hardcoded machine USB/serial topology.

This is a productized vendor snapshot. It is not an accepted XGC low-polygon
visual default.

| Item | Value |
|------|--------|
| ROS package | `g1_description` |
| Visual URDF | `urdf/g1_visual.urdf` |
| Robot name | `g1` |
| Canonical source | g1_29dof_with_hand_rev_1_0 (up-to-date full model) |
| Debian package | `ros-noetic-xgc2-g1-description` |

Meshes and kinematics remain Unitree's (BSD-3-Clause). Mesh paths use
`package://g1_description/meshes/...`.

## Build

```bash
source /opt/ros/noetic/setup.bash
catkin_make_isolated --pkg g1_description
```

## Install

```
sudo apt update
sudo apt install ros-noetic-xgc2-g1-description
```

## Use

```text
$(rospack find g1_description)/urdf/g1_visual.urdf
```

Joint states and TF still come from drivers; this package only supplies
description assets.
