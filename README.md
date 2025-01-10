
# Autonomous Rover 

This project involves developing a fully autonomous rover capable of reaching a specific target location while following a sample using object detection. The rover employs a custom path-planning algorithm to navigate. If obstacles are detected along the path, the rover avoids them dynamically. Additionally, if the rover cannot directly follow the sample's path, it uses an EKF (Extended Kalman Filter) for localization based on IMU and wheel odometry to reach the target coordinates.




 Index

    1. Features
    2. Hardware Requirements
    3. Software Requirements
    4. Run Code
    5. Demo
## Features

- Autonomous navigation using a custom path-planning algorithm.
- Real-time object detection with YOLOv8.
- Dynamic obstacle avoidance.
- Localization using EKF with IMU and wheel odometry.
- Integration with ROS 2 Humble framework.



## Hardware Requirements

- Depth Camera (IntelRealsense D435)
- Web camera (Logitech)
- Processor (Skull saints -Venom )
- Robotic arm 
- Planetary motors
- Motor Driver 
- IMU Sensor 
- Batteries (Roving and Arm)

## Software Requirements
- Ubuntu 22.04
- ROS 2 Humble
- Python 3.x
- Intel RealSense SDK
- PyTorch
- OpenCV 
- Additional dependencies (listed in requirements.txt)
- EKF Filter Packages




## Run Locally

Clone the project

```bash
  git clone https://link-to-project
```

Go to the project directory

```bash
  cd ~/dev_ws
```

Install dependencies

```bash
  pip install -r requirements.txt
  sudo apt install ros-humble-tf-transformations
  sudo apt install ros-humble-robot-localization
```

Set up the rover at its initial coordinates (0, 0, 0)

Launch the project using the following command:

```bash
  ros2 launch basic_mobile_robot LAUNCH.py
```


## Demo



