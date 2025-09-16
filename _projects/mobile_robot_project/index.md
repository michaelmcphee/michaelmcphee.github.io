---
layout: post
title: Autonomous Differential Drive Robot
description: A two-wheeled differential drive robot designed for testing and validating a Kalman filter algorithm for real-time localization.
skills:
  - SolidWorks
  - MATLAB
  - Arduino
  - Kalman Filtering
  - Mobile Robot Localization
  - PID Control
  - 3D Printing
  - Sensor Integration
  - I²C Communication
  - PWM Motor Control
  - Electronics Wiring
main-image: /assets/images/robot-photos/robot.png
---

## Design Objectives
- Fully design the robot’s mechanical system in SolidWorks, including chassis, drivetrain, and sensor mounts.  
- Assemble and integrate electrical systems: battery pack, motor drivers, custom I²C breakout board, and wiring.  
- Test motors and sensors using Arduino for accurate real-world data collection.  
- Develop and implement a Kalman filter for real-time localization, including:  
  - A **system model** describing robot dynamics with state vector and state transition matrix.  
  - An **observation model** mapping sensor inputs (encoders, IMU) to measurable states.  
- Provide validated models and hardware to support a future FPGA-based demonstration of high-performance Kalman filtering.

## Outcomes
- Completed the full SolidWorks design and 3D-printed all custom mechanical components.  
- Successfully assembled and tested all mechanical and electrical systems.  
- Verified sensor and motor performance using Arduino for reliable data collection.  
- Developed a **robust Kalman filter** in MATLAB with fully-defined system and observation models for accurate mobile robot localization.  
- Generated validated state-space and observation models, enabling real-time localization and supporting future FPGA integration.  

## Technical Details
### Electronics
<div class="section-flex">
  <div class="text">
    <ul>
      <li>Battery pack: 3×18650 Li-ion cells in series (12 V nominal) with modular DIN rail mounting.</li>
      <li>Motor controller: L298N dual H-bridge with PWM speed control and logic-level interfacing.</li>
      <li>AS5048B magnetic rotary encoders and optional IMU for precise motion tracking.</li>
      <li>Custom I²C breakout board to distribute 3.3 V, GND, SCL, and SDA lines to multiple devices.</li>
    </ul>
  </div>
  <div class="image">
    <img src="/assets/images/robot-photos/robot_electronics.png" alt="Robot electronics" />
  </div>
</div>

---

### Software
<div class="section-flex">
  <div class="text">
    <ul>
      <li><strong>MATLAB implementation of Kalman filter</strong> for mobile robot localization, using:
        <ul>
          <li><strong>System model</strong> capturing the robot’s dynamics with state vector [x, y, θ, v, ω].</li>
          <li><strong>Observation model</strong> mapping encoder and IMU readings to measurable states.</li>
        </ul>
      </li>
      <li>Real-time localization validated with sensor data collected from the Arduino prototype.</li>
      <li>PID control for velocity and position regulation based on filtered state estimates.</li>
      <li>Arduino C/C++ for motor control, sensor interfacing, and data logging.</li>
    </ul>
  </div>
  <div class="image">
    <img src="/assets/images/robot-photos/robot_matlab.png" alt="MATLAB Kalman filter" />
  </div>
</div>

---

### Mechanical
<div class="section-flex">
  <div class="text">
    <ul>
      <li>SolidWorks CAD for complete chassis, drivetrain, and sensor mounts.</li>
      <li>3D-printed brackets for motors, wheels, and encoders, optimized for stability and alignment.</li>
      <li>Aluminum extrusion frame with DIN rail for modular electronics mounting.</li>
      <li>Modular design allows easy adjustments, debugging, and future expansions.</li>
    </ul>
  </div>
  <div class="image">
    <img src="/assets/images/robot-photos/robot_solidworks.png" alt="SolidWorks CAD" />
  </div>
</div>
