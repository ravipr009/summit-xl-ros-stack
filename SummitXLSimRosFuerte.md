# Packages of the SummitXL stack #

**robotnik\_worlds**

This package contains .world .inc files to define the Robotnik offices world to be used in simulation.

**summit\_xl\_2dnav**

This package contains all the configuration files needed to execute the AMCL and SLAM navigation algorithms in simulation.

**summit\_xl\_ctrl**

Robot Gazebo plugin controller. Implements the control of the Skid-steering kinematics of the SummitXL robot. Will include different types of wheels soon.

**summit\_xl\_description**

The urdf, meshes, and other elements needed in the description are contained here.
Note that the ackerman steering contains several closed kinematic chains that have been simulated by single joints with a type of 'electronic gearing' of the controller.

**summit\_xl\_exploration**
Adaption of the demos done by Charles DuHadway, Benjamin Pitzer for the bosch-ros-pkg but using the SummitXL robot and our environment.

**summit\_xl\_joystick**

This package allows using a joystick gamepad (PS3, Logitech, Thrustmaster, etc.) with the summit\_xl\_ctrl, sending the messages received through the joystick input, correctly adapted, to the "summit\_xl\_ctrl" command topic.

**summit\_xl\_odometry**

Computes the odometry of the robot using the same procedure as the robot, i.e. using the joint movements and a IMU. Publish these odometry to /odom. May be feedbacked with a kalman filter to obtain a better trasformation through /map and /odom frame.

**summit\_xl\_sbpl\_nav**

Use of the sbpl and sbpl\_lattice\_planner to create navigation plans. Planning restricted to skid-steering kinematics. The pose following works perfectly for the SummitXL kinematics.