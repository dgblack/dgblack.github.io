## Robotics and Control Lab (RCL) Coop
#### Date: May - December 2019

I did an 8 month internship in Dr. Tim Salcudean’s lab at the University of British Columbia in 2019, working towards a haptic feedback system for the da Vinci surgical robot. I redesigned the wrist of the master arm to integrate a force sensor with minimal impact on the robot’s kinematics or dynamics. I also implemented various experiments and applications using the design and the robot’s complex teleoperation and control systems. This involved mechanical and electrical design and prototyping, working with Robot Operating System (ROS), C++, Python, and MATLAB, as well as kinematics, and dynamic model identification. I also helped design a real-time communication and control system for a novel 6-axis force/torque sensor with IMU and temperature sensing.

The RCL Lab works closely with Intuitive to perform groundbreaking research with the da Vinci Robot. As such, we were given two master manipulators. I first designed and built a simple frame to mount the two arms (Master Tool Manipulaters, i.e. MTMs):

![MTM Frame](/images/frame.jpg)
<img src="/images/frame.jpg" alt="MTM Frame"
	width="400" height="500" />
![MTM Arms](/images/arms.jpg)

I then began reverse-engineering the MTM wrist yaw link, and modified mechanically and electrically it to integrate a 6-axis ATI Nano43 force/torque sensor without changing the kinematics of the robot. This involved complex CAD modelling and a variety of manufacturing processes as we went through a number of prototypes, trying to fine-tune the rigidity, weight and tolerances to minimize impact on friction, flexing, and inertia, and thus the robot dynamics and operator feel.

##### One idea in CAD
![MTM Wrist CAD](/images/cad.png)

##### Result of attempting to waterjet cut the part
![MTM Wrist Waterjet](/images/VID_20190702_081911.mp4)

##### The final part, with electrical modifications
![MTM Wrist Open](/images/wristOpen.jpg)
![MTM Wrist](/images/wrist.jpg)

