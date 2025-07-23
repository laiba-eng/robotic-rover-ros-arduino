# robotic-rover-ros-arduino
A semi-autonomous 4-wheel robotic rover for academic monitoring, implemented using ROS and Arduino for differential drive control without sensors.

# Features
- 4-wheel rover structure modeled using URDF with XACRO macros
- Motion control via ROS Python node (`square_drive.py`)
- Arduino-based motor control receiving velocity commands from ROS
- Simulated and tested in Gazebo

# Architecture Overview
This project integrates hardware and software to control a differential-drive robotic rover using ROS and Arduino. The architecture is divided into two layers:
# Software Layer (ROS)
- The system is developed using ROS (Robot Operating System) on Ubuntu, hosted via VMware.
  
- A custom Python script (e.g., square_drive.py) publishes velocity commands to the /cmd_vel topic using geometry_msgs/Twist messages.

- These commands are transmitted to the Arduino Uno via serial communication.

- The Arduino interprets the commands and controls the motors using an L298N motor driver to drive the rover in predefined patterns.

# Hardware Layer
- The Arduino Uno receives velocity commands through its serial port.

- Based on these commands, it controls the motors using an L298N motor driver.

- No sensors are used; movement is open-loop and predefined.
  
# Simulation
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/322868f1-7452-4027-bea8-a845d3bc5450" />
RViz Simulation

<img width="250" height="250" alt="image" src="https://github.com/user-attachments/assets/725a26f0-9cbd-4058-8d93-9a83c22c9cfd" />
<img width="250" height="250" alt="image" src="https://github.com/user-attachments/assets/9bd69838-fcb2-4361-a6cb-70a8315e3404" />
Gazebbo Simulation


