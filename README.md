Documentation is at https://index.ros.org/doc/ros2/

```
vcs import src < ros2_ex.repos
```
```
rosdep install  --rosdistro  foxy  --from-paths src --ignore-src -y --skip-keys "fastcdr rti-connext-dds-5.3.1 urdfdom_headers realsense2_description realsense2_camera realsense2_description  "
```
