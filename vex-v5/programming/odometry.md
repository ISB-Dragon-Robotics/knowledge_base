---
description: By George Xu (ISB)
---

# Odometry

## Introduction

As discussed in the previous page, it is easy for simple scripts to break as those methods are unreliable due to real-world inconsistencies like wheel slippage and motor variation. Odometry, the application of the methods discussed, provides a far more accurate method by tracking the robot’s movement in real-time.

Odometry works by continuously updating the robot’s position using wheel encoders, free-spinning wheels which are used to measure motion, and other sensors. This enables the robot to “know” where it is on the field at any given time, significantly improving the consistency of autonomous movement.

## **Odometry System Components**

A proper odometry system requires two key components

First, they have the tracking wheels, often called free-spinning or dead wheels. These wheels are not attached to a motor and are instead placed in contact with the ground. Often, a suspension-like system of rubber bands may be used to apply a downward force, preventing slippage. Encoders, devices that can detect movement or rotation, are used to measure movement. VEX provides Optical Shaft Encoders and V5 Rotation Sensors, both of which can be used to measure the wheel rotation

If preferred, it is possible to combine this with an Inertial Sensor, such as an IMU or Gyroscope, which can measure the robot's heading, reducing errors and drift.

## Standard Odometry Setup

If only two dead wheels are used, the following two methods can be considered. The first setup uses two wheels facing the forward direction. When moving in one direction, the rotation of these dead wheels can be used to calculate the distance traveled. However, this is disadvantageous as it cannot take into account sideways slippage.

Alternatively, a forward-facing and a perpendicular dead wheel can be used. The forward-facing wheel is best placed along the central axis (forward-facing) of the base. If not, the offset must be considered when computing the rotational movement of the robot. The perpendicular wheel should be placed along the central axis of the robot, though offset from the center. The further away it is from the center, the lower the error of the measurement. This design is largely functional but risks errors.

If three wheels are used, two forward-facing and one perpendicular wheel can be used, minimizing issues.

## **How Odometry Works**

Odometry continuously calculates the robot’s position by using wheel encoder data and integrating the displacement over time. This process follows a set of mathematical equations that estimate movement. They are implemented in the following steps. Step one is useful in a match but not necessary to understand the process of Odometry

### Step 1: Reset the position

This can be done by coding the robot to align itself at a corner or by simply placing it in an appropriate position.

Now, there are 3 cases, each for a different set of Odometry wheels.

We will set the following coordinate system:

$$
(x,y,\theta)
$$

Where x is the sideways coordinate, y is the forward/backward coordinate, and theta is the angle the robot points to.

### **Case 2: Two Forward Wheels**

Track the relevant wheels, as to be discussed below

### **Step 3: Calculations**

#### **Case 1: Two Forward Wheels**

Let's term ΔL and ΔR as the two forward wheel displacements. If your encoder gives an angle, you will need to multiply the angle by the wheel radius. We also define track width as the distance between the two dead wheels. We first compute local variables before adding them to the global coordinates:

$$
\Delta a = \frac{\Delta L + \Delta R}{2} \qquad \Delta b = \frac{\Delta L - \Delta R}{Track \,\, Width}
$$

$$
\Delta \theta = \Delta b \qquad \Delta x = -\Delta a \sin(b) \qquad \Delta y = \Delta a \cos(b)
$$

#### Case 2: One Forward and One Side Wheel

Let's term ΔF and ΔS as the forward and side wheel displacements, respectively. We also define radius as the distance between the side wheel and the robot's center of rotation. Again, we first find local variables and then global coordinates.&#x20;

$$
\Delta a = \Delta F \qquad \Delta b = \Delta S \qquad
$$

$$
\Delta \theta = \frac{\Delta S}{Radius} \qquad \Delta x = \Delta b \cos(\theta) - \Delta a \sin(\theta) \qquad \Delta y = \Delta b \sin(\theta) + \Delta a \cos(\theta)
$$

#### Case 3: 2 Forward Wheels and One Side Wheel

Let's term ΔL, ΔR, and ΔS as the two forward wheel displacements.

$$
\Delta a = \frac{\Delta L + \Delta R}{2} \qquad \Delta b = \Delta S \qquad \Delta c = \frac{\Delta L - \Delta R}{Track \,\, Width}
$$

$$
\Delta \theta = \Delta c \qquad \Delta x = \Delta b \cos(c) - \Delta a \sin(c) \qquad \Delta y = \Delta b \sin(c) + \Delta a \cos(c)
$$

### **Step 4: Update Position**

The new global position is obtained by adding the global displacements to the current position. Using this, the script may recalculate the path and feed back into the PID controller. For ISB students, the Lead Programmer should have an example script.

## **Advanced Techniques**

To reduce error, combining difference sensors may be optimal. For example, using gyros for heading and encoders for position. Additionally, using a GPS sensor may allow periodic corrections. Beyond the autonomous phase, this can even be used during manual control. By linking controller instructions with this script, damages to the base, such as sudden increases in friction or any other issues that may disproportionately affect one side of the base, may be correct for by quickly adjusting the max speed of one side's motors.

Also, this may be added to X-drive or mecanum robots, but adjustments must be made for more accurate omnidirectional movement control. Make sure to experiment with any designs before using them in-game
