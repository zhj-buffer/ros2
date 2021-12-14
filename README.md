Documentation is at https://index.ros.org/doc/ros2/

Follow the ROS2 guide first to install all the requirements.


```
vcs import src < ros2_ex.repos
```

```
rosdep install  --rosdistro  foxy  --from-paths src --ignore-src -y --skip-keys "fastcdr rti-connext-dds-5.3.1 urdfdom_headers "
```


```
nvidia@nvidia-desktop:~$ ls /usr/lib/aarch64-linux-gnu/libssl.so* -lh
lrwxrwxrwx 1 root root   13 Nov 24 21:50 /usr/lib/aarch64-linux-gnu/libssl.so -> libssl.so.1.1
-rw-r--r-- 1 root root 355K Aug 25 00:16 /usr/lib/aarch64-linux-gnu/libssl.so.1.0.0
-rw-r--r-- 1 root root 488K Nov 24 21:50 /usr/lib/aarch64-linux-gnu/libssl.so.1.1
nvidia@nvidia-desktop:~$ sudo cp /usr/lib/aarch64-linux-gnu/libssl.so.1.1 /usr/lib/aarch64-linux-gnu/libssl.so.1.0.0 /usr/local/lib/


nvidia@nvidia-desktop:~$ sudo ln -s /usr/local/lib/libssl.so.1.1 /usr/local/lib/libssl.so
nvidia@nvidia-desktop:~/workspace/ros2$ sudo cp /usr/lib/aarch64-linux-gnu/libcrypto.so.1.1 /usr/lib/aarch64-linux-gnu/libcrypto.so.1.0.0 /usr/local/lib/
nvidia@nvidia-desktop:~/workspace/ros2$ sudo ln -s /usr/local/lib/libcrypto.so.1.1 /usr/local/lib/libcrypto.so
```

```
colcon build --merge-install
```
