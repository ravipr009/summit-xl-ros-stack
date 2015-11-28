#Packages of the SummitXL stack (Groovy)

# Packages of the SummitXL stack #

This metapackage includes the simulation for the Summit XL series rovers (Summit XL, Summit XL OMNI and X-WAM)

The summit\_xl\_sim simulation stack is composed of the following packages:

**summit\_xl\_description**

The urdf, meshes, and other elements needed in the description are contained here. The standard camera configurations have been included (w/wo sphere\_camera, w/wo axis\_camera, etc.). This package includes the description of the Summit XL, Summit XL OMNI and X-WAM mobile platforms.
The package includes also some launch files to publish the robot state and to test the urdf files in rviz.

**summit\_xl\_gazebo**

This package defines the launch files for launching the models contained in the previous package in gazebo. This package contains also world definitions for gazebo.

**summit\_xl\_control**

This package contains the launch and configuration files to spawn the joint controllers with the ROS controller\_manager. It allows to launch the joint controllers for the Summit XL (4 axes skid steering + 2 axes ptz), Summit XL OMNI (4 axes skid steering, 4 axes swerve drive), Summit X-WAM (4 axes skid steering, 4 axes swerve drive, 1 linear axis for scissor mechanism).

The Summit XL simulation stack follows the gazebo\_ros controller manager scheme described in
http://gazebosim.org/wiki/Tutorials/1.9/ROS_Control_with_Gazebo

**summit\_xl\_robot\_control**

This controller. implements the control of the 4 axes - skid-steering kinematics of the Summit XL robot and Omnidirectional kinematics of the Summit XL Omni and X-WAM robots. It reads the joint states from the published joint\_state and sends the appropriate references to each axis according to the subscribed commands. The commands can be sent from the summit\_xl\_joystick, summit\_xl\_2dnav or any other package.

This node also computes the odometry of the robot using the joint movements and a IMU. Publish these odometry to /odom. The node has a flag in the yaml files that forces the publication or not of the odom->base\_footprint frames, needed by the localization and mapping algorithms.

**summit\_xl\_2dnav**

This package contains all the configuration files needed to execute the AMCL and SLAM navigation algorithms in simulation.

**summit\_xl\_joystick**

This package allows to use a joystick with the summit\_controller, sending the messages received through the joystick input, correctly adapted, to the "/summit\_xl\_robot\_control/command" topic.

**summit\_xl\_waypoints**

This package uses the move\_base stack in order to send sequences of goals to the rover.

**summit\_xl\_joint\_state**

Simple template (example) to access the joint states.
