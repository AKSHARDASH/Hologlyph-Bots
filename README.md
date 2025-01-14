# Hologlyph Bots Project

Welcome to the Hologlyph Bots project! This repository contains the code and resources for a team of three holonomic drive robots designed to create large drawings resembling geoglyphs. The robots coordinate with each other using an overhead camera and are controlled via ROS2 and micro-ROS.


Credits AKSHAR DASH,ROHAN MOHAPATRA,ANUP KUMAR NAYAK,CH PREMSAI PATRO 
![IMG-20240311-WA0014](https://github.com/AKSHARDASH/Hologlyph-Bots/assets/134735494/3ad60f60-9bc0-40c7-b1d2-5fadb639e8d0)
![IMG-20240311-WA0016](https://github.com/AKSHARDASH/Hologlyph-Bots/assets/134735494/0e0322c6-b0f7-4172-85dc-1ba296305be4)

![image](https://github.com/AKSHARDASH/Hologlyph-Bots/assets/134735494/f16bab98-53c4-4d3a-bc44-b458c90e8522)
![image](https://github.com/AKSHARDASH/Hologlyph-Bots/assets/134735494/211f872a-febb-43d8-89fd-15b9aed8ff21)

## Table of Contents
1. [Introduction](#introduction)
2. [Project Structure](#project-structure)
3. [Setup Instructions](#setup-instructions)
4. [Usage](#usage)
    - [Function Mode](#function-mode)
    - [Image Mode](#image-mode)
5. [Localization](#localization)
6. [Pen Mechanism](#pen-mechanism)
7. [Demonstration](#demonstration)


## Introduction
The Hologlyph Bots project aims to create intricate drawings by coordinating three holonomic drive robots. The robots are localized using Aruco markers and controlled through an overhead camera system. Each robot is equipped with a pen mechanism connected to a servo motor, allowing them to draw on a surface.

## Project Structure
- **ros2_package/**: Contains the final ROS2 package for controlling the robots.
- **microros_script/**: Contains the micro-ROS script uploaded on the ESP32 for robot control.

## Setup Instructions
1. **Clone the Repository:**
    ```bash
    git clone https://github.com/yourusername/hologlyph-bots.git
    cd hologlyph-bots
    ```

2. **Install Dependencies:**
    - ROS2: Follow the official [ROS2 installation guide](https://docs.ros.org/en/foxy/Installation.html).
    - Micro-ROS: Refer to the [micro-ROS documentation](https://micro.ros.org/docs/tutorials/).

3. **Build the ROS2 Package:**
    ```bash
    cd ros2_package
    colcon build
    source install/setup.bash
    ```

4. **Upload the micro-ROS Script:**
    - Connect the ESP32 to your computer.
    - Navigate to the `microros_script` directory and follow the upload instructions.

## Usage
The robots can operate in two different modes: Function Mode and Image Mode.

### Function Mode
In Function Mode, the robots follow pre-defined mathematical functions to create drawings. To start this mode:
```bash
ros2 launch hologlyph_bots function_mode.launch.py
```

### Image Mode
In Image Mode, the robots use an image file to guide their drawing. To start this mode:
```bash
ros2 launch hologlyph_bots image_mode.launch.py
```

## Localization
The robots are localized using Aruco markers. Ensure that the markers are placed correctly in the environment and are visible to the overhead camera. The localization node will process the camera feed to determine the positions of the robots.

## Pen Mechanism
Each robot is equipped with a pen mechanism controlled by a servo motor. The pen can be raised or lowered based on the drawing commands received from the ROS2 nodes.

## Demonstration

[Video Demonstration 1](https://www.youtube.com/watch?v=NF9OK72-EHQ)




[Video Demonstration 2](https://youtu.be/E1_FC1jOoHo)


#THANK YOU
