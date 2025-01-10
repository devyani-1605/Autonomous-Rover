Autonomous Rover 
This project involves developing a fully autonomous rover capable of reaching a specific target location while following a sample using object detection. The rover employs a custom path-planning algorithm to navigate. If obstacles are detected along the path, the rover avoids them dynamically. Additionally, if the rover cannot directly follow the sample's path, it uses an EKF (Extended Kalman Filter) for localization based on IMU and wheel odometry to reach the target coordinates.

Table of Contents
    1. Features
    2. Hardware Requirements
    3. Software Requirements
    4. Install Dependencies
    5. Setup and Usage
    6. Run Code
    7. Calibrate Sensors
    8. Notes

Features
    • Autonomous navigation using a custom path-planning algorithm.
    • Real-time object detection with YOLOv8.
    • Dynamic obstacle avoidance.
    • Localization using EKF with IMU and wheel odometry.
    • Integration with ROS 2 Humble framework.

Hardware Requirements
    • Rover with the following components:
        ◦ Depth Camera (IntelRealsense D435)
        ◦ web camera (Logitech)
        ◦ processor (Skull saints -Venom )
        ◦ Robotic arm 
        ◦ Planetary motors
        ◦ Motor Driver 
        ◦ IMU Sensor 
        ◦ Batteries

Software Requirements
    • ROS 2 Humble
    • Python 3.x
    • Intel RealSense SDK
    • PyTorch
    • OpenCV
    • Additional dependencies (listed in requirements.txt)
    • EKF Filter Packages:
      sudo apt install ros-humble-tf-transformations
      sudo apt install ros-humble-robot-localization

Install Dependencies
    1. Clone the repository:
       git clone <repository-url>
       cd <repository-folder>
    2. Install Python dependencies:
       pip install -r requirements.txt

Setup and Usage
    1. Set up the rover at its initial coordinates (0, 0, 0).
    2. Navigate to the development workspace:
       cd ~/dev_ws
    3. Build the ROS 2 workspace:
       colcon build

Run Code
Launch the project using the following command:
ros2 launch basic_mobile_robot LAUNCH.py

Calibrate Sensors
    • IMU Calibration: Ensure the IMU is properly aligned and calibrated before running the code.
    • Camera Calibration: Verify that the Intel RealSense camera is calibrated for intrinsic and extrinsic parameters.
    • Wheel Odometry: Ensure the wheel encoders are configured correctly for accurate distance measurement.

Notes
    • Ensure all hardware components are securely connected and operational before running the code.
    • For troubleshooting, refer to the ROS 2 and YOLOv8 documentation as needed.
    • Adjust path-planning and obstacle-avoidance parameters in the configuration files if necessary.
