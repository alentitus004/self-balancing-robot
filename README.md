# Self-Balancing Two-Wheeled Robot

This is a two-wheeled robot that balances itself upright, based on the inverted pendulum principle. I built it to learn how real-time control actually works on hardware, and honestly, getting it to stand without falling over took a lot more tuning than I expected.

## What it does

The robot reads its own tilt using an MPU6500 IMU. The accelerometer and gyroscope readings are combined with a complementary filter to get a stable angle. The Arduino UNO runs a PID controller on that angle and tells the motors which way to move to stop the robot from falling. Wheel encoders keep track of how far the wheels have moved.

## Goals

- Build a two-wheeled self-balancing robot
- Estimate tilt angle with the MPU6500
- Use PID control to correct balance in real time
- Use a complementary filter for sensor fusion
- Use encoder feedback to monitor wheel movement

## Hardware

- Arduino UNO
- MPU6500 IMU
- 12V DC geared motors with encoders
- Cytron dual motor driver
- Rechargeable battery
- Chassis and wheels

## Problems I ran into

- Noise and drift in the IMU readings
- Motor dead zones, and the two motors not responding the same way
- Interference on the encoder signals
- PID tuning (this took the longest)
- Getting the weight distribution right on the chassis

## What I want to add next

- A load sensor to detect when the robot falls or gets lifted
- Better motion control using the encoder feedback
- Wireless control and live monitoring

## Tech used

Embedded C/C++ (Arduino), PID control, sensor fusion, encoder feedback, robotics and mechatronics
