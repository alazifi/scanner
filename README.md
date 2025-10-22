# TRUSMI LIDAR ROS2 Package

TRUSMI LIDAR ROS2

## How to install ROS2

[humble](https://docs.ros.org/en/humble/Installation.html)

## How to configuring your ROS 2 environment

[Configuring your ROS 2 environment](https://docs.ros.org/en/humble/Tutorials/Configuring-ROS2-Environment.html)

## How to Create a ROS2 workspace

[ROS2 Tutorials Creating a workspace](https://docs.ros.org/en/humble/Tutorials/Workspace/Creating-A-Workspace.html)

1. example, choose the directory name ros2_ws, for "development workspace" :

   ```bash
   mkdir -p ~/ros2_ws/src
   cd ~/ros2_ws/src
   ```

## Compile & Install rplidar_ros package

1. Clone rplidar_ros package from github

   Ensure you're still in the ros2_ws/src directory before you clone:

   ```bash
   git clone -b ros2 https://github.com/alazifi/scannery.git
   ```

2. Build rpidar_ros package

   From the root of your workspace (ros2_ws), you can now build rplidar_ros package using the command:

   ```bash
   cd ~/ros2_ws/
   source /opt/ros/<rosdistro>/setup.bash
   colcon build --symlink-install
   ```

   if you find output like "colcon:command not found",you need separate [install colcon](https://docs.ros.org/en/foxy/Tutorials/Colcon-Tutorial.html#install-colcon) build tools.

3. Package environment setup

    ```bash
    source ./install/setup.bash
    ```

    Note: Add permanent workspace environment variables.
    It's convenientif the ROS2 environment variables are automatically added to your bash session every time a new shell is launched:

    ```bash
    $echo "source <your_own_ros2_ws>/install/setup.bash" >> ~/.bashrc
    $source ~/.bashrc
    ```

## Run rplidar_ros

### Run rplidar node and view in the rviz

The command for LIDAR is :

```bash
ros2 launch rplidar_ros view_rplidar_t1_launch.py
```

Notice: different lidar use different serial_baudrate.

## RPLIDAR frame

RPLIDAR frame must be broadcasted according to picture shown in rplidar-frame.png
