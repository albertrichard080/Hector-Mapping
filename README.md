# Hector Mapping Readme

# Introduction

Hector Mapping is another ROS-compatible mapping tool designed for robotic applications.It doesn't need odometry information.This readme provides guidance on integrating Hector Mapping with an RPLidar sensor. Follow the steps below for a successful setup.
# Prerequisites

Before proceeding, ensure you have obtained the necessary permissions for the RPLidar sensor's port. Grant permission using the following command:

bash

    sudo chmod 666 /dev/ttyUSB0

Replace /dev/ttyUSB0 with the correct port on your system.
# Launching RPLidar

Navigate to your ROS workspace directory. In the provided example:

bash

    cd ~/richard/src/rplidar_ros/launch/

Launch the RPLidar node using the appropriate launch file, e.g., rplidar.launch:

bash

    roslaunch rplidar.launch

Ensure that the RPLidar initializes successfully, and make a note of the assigned serial port.
# Launching Hector Mapping

Open a new terminal and navigate to the ROS workspace directory:

bash

    cd ~/richard/src/Hector_mapping-and-rplidar/Hector-Mapping/hector_slam_launch/launch/

Launch Hector Mapping using the provided launch file, for example:

bash

    roslaunch hectormap.launch

# Launching Map Saver

To save the map run the following command:

bash

    rosrun map_server map_saver -f map

Ensure the sequence is followed meticulously for accurate mapping results. Refer to the ROS documentation or community forums for troubleshooting or additional information.
Ensure Hector Mapping initializes and begins processing data from the RPLidar sensor.
# Additional Notes

  Ensure that /dev/ttyUSB0 is replaced with the correct port assigned to your RPLidar.
  Adjust file paths based on your ROS workspace structure.
  Refer to the Hector Mapping documentation for advanced configurations and troubleshooting.
  Consult RPLidar documentation for any sensor-specific requirements.
