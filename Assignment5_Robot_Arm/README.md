# Assignment 5: Robot Arm Start-up Check

## Overview
This project implements a robot arm start-up system using ROS 2 Jazzy and Python. The system consists of three ROS 2 nodes that communicate through services to check the battery, calibrate the sensor, enable the motors, and control the vacuum.

## Nodes

### 1. Power Node
- Starts with a battery level of 100%.
- Decreases the battery by 5% every 3 seconds.
- Provides a service to check the battery level.
- Provides a service to charge the battery back to 100%.

### 2. Arm Node
- Calibrates the sensor.
- Enables or disables the motors.
- Controls the vacuum ON/OFF state.
- Prevents the motors from being enabled before sensor calibration.

### 3. Startup Node
Automatically performs the following sequence:

1. Check battery level.
2. Calibrate the sensor.
3. Enable the motors.
4. Turn the vacuum ON.
5. Turn the vacuum OFF.

If any step fails, the startup process stops and reports the failure. When all steps succeed, the system displays `Arm ready`.

## Technologies Used
- ROS 2 Jazzy
- Python
- ROS 2 Services
- `rclpy`
- `std_srvs`

## Testing
The system was tested under the following scenarios:

- Successful robot arm startup.
- Startup failure due to low battery.
- Battery charging and successful recovery.

## Submission Files
- `arm_robot.zip` — ROS 2 package source files.
- `Assignment5_Report.pdf` — Report containing screenshots and test results.

---

**Course:** Robotics Operating Systems  
**Student:** Dana Ahmad Zakarna
