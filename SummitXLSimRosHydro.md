# Packages of the SummitXL stack #

**bh262\_description**

Contains the description of the Barrett Hand: urdf and meshes. This Hand is mounted on the WAM arm and is the end effector used by the [X-WAM mobile manipulator](http://www.robotnik.es/en/products/mobile-manipulators/x-wam).


**summit\_xl\_2dnav**

This package contains all the configuration files needed to execute the AMCL and SLAM navigation algorithms in simulation.


**summit\_xl\_control**

New gazebo 1.9 style robot control

**summit\_xl\_description**

robot description (urdf and meshes). Includes also V-REP model.

**summit\_xl\_gazebo**

launch files and world files to start the models in gazebo

**summit\_xl\_joint\_state**

test node to publish joint states (as alternative to the joint\_state\_publisher)

**summit\_xl\_joystick**

node to process the joystick in simulation (configured for PS3, but others are also possible).

**summit\_xl\_robot\_control**

control the robot joints in all kinematic configurations, publishes odom topic and, if configured, also tf odom->base\_link. Usually takes as input joystick commands and generates as outputs references for the gazebo controllers defined in summit\_xl\_control.

**summit\_xl\_waypoints**

pass a set of goals from a file to the move\_base stack.

**wam\_description**

Barrett WAM (Whole Arm Manipulator) urdf and meshes.

**xl\_terabot\_description**

Robot description of the [XL-Terabot robot](http://www.robotnik.es/en/products/mobile-manipulators/xl-terabot).

**x\_wam\_moveit**

Draft moveit package to control the X-WAM.