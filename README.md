# **PITA: BalanceBot**

**PITA** is a simple two-wheeled self-balancing robot that can be controlled via an Android app. It uses an Arduino to control the motors and sensors, and the Android app is made using Flutter to move and rotate the bot.
I built this project as part of my bachelor's program in 2020.

## Overview

The **PITA** uses a PID controller to keep itself balanced. The PID controller constantly measures the angle of the robot using the MPU6050 sensor. If the bot tilts forward or backward, the PID controller adjusts the speed of the motors to bring the bot back to its upright position. This makes sure the robot doesn’t fall over and stays balanced while stationary or moving.

### Controlling the Movement

To make the robot move forward or backward, we change the balance point of the robot by slightly shifting it away from its center of mass. When the bot starts to "fall" in one direction, the controller tries to bring it back to balance, which results in forward or backward movement. Essentially, the robot is constantly falling and correcting itself, making it move.

For turning, the robot doesn't need to tilt. Instead, we control the speed of each wheel. To turn left, we slow down the left wheel and to turn right, we slow down the right wheel. This difference in wheel speeds causes the robot to rotate in the desired direction.

### Note

To achieve better results, use stepper motors or DC motors with high-quality encoders. Controlling DC motors without any feedback, such as encoders, and relying solely on angle data can be challenging.

## Parts Used

- Aluminium plates and screw rods (for the frame)
- Arduino UNO
- MPU6050 module (Gyroscope and Accelerometer)
- L298N module (Motor Driver)
- DC Motors with gearbox
- HC-06 Bluetooth module

## Initial Test Run

![Initial Test Run Video](assets/initial-test-run.gif)

## Images

### Bot overview

<div>
    <img src="assets/overview.jpg" alt="Bot overview" width="600" />
    <p><em>Figure 1. Bot overview (at development time)</em></p>
</div>

### Remote control

<div>
    <div>
        <img src="assets/app-01.png" alt="Remote control app" width="200" />
        <img src="assets/app-02.png" alt="Remote control app" width="200" />
        <img src="assets/app-03.png" alt="Remote control app" width="200" />
    </div>
    <div>
        <img src="assets/app-04.png" alt="Remote control app" width="200" />
        <img src="assets/app-05.png" alt="Remote control app" width="200" />
        <img src="assets/app-06.png" alt="Remote control app" width="200" />
    </div>
    <p><em>Figure 2. Remote control application</em></p>
</div>
