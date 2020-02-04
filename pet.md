# Robotic, Anthorpomorphic PET Phantom

For my first capstone project (engineering physics' analogue to a thesis project in an honors physics degree, except we do two), I worked in a team of three with the BC Cancer Research Centre. We designed and built a robotically actuated, physiologically accurate, anthropomorphic phantom for use in PET motion correction studies. This involved mechatronic design, fluid dynamics, and PET physics, as well as project management skills in an interdisciplinary team of engineers, biologists, and physicists.

To achieve anatomical accuracy, it was important to consider the material attenuation coefficients to match human soft tissue, lung, and bone under x-ray and gamma radiation. We designed a set of flexible, inflatable, anatomically realistic lungs by molding a liquid silicone elastomer onto 3D printed lungs obtained from a CT scan. These lungs are positioned inside a realistic ribcage and torso shell, and actuated using a rubber diaphragm membrane and linear actuator. The linear actuator is controlled by a PID algorithm running on a Raspberry-PI.

#### Phantom Torso with Ribcage
![Phantom](/images/phantomInBox.jpg)

#### Phantom with Diaphragm Membrane, Linear Actuator, and Lungs
![Phantom](/images/basePlateAssem.jpg)

One of the first things we did was prototype (using a waterjet cutter) and test the diaphragm membrane. The CAD models for the base plate onto which the diaphragm attaches were derived from a CT scan of the phantom torso to get as accurate dimensions as possible.

#### Diaphragm Prototype
![Diaphragm Prototype](/images/prototypeDiaphragm.jpg)
