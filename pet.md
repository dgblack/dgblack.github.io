# Robotic, Anthorpomorphic PET Phantom

For my first capstone project (engineering physics' analogue to a thesis project in an honors physics degree, except we do two), I worked in a team of three with the BC Cancer Research Centre. We designed and built a robotically actuated, anatomically accurate, anthropomorphic phantom for use in studies on the effect of respiratory motion on PET image quantification and reconstruction. This involved mechatronic design, fluid dynamics, and PET physics, as well as project management skills in an interdisciplinary team of engineers, biologists, and physicists. To fabricate the parts, we used 3D-printing, waterjet cutting, milling, and silicone rolling techniques. Additionally, we produced engineering drawings for a machine shop to manufacture the piston and cylinder. 

We decided to open source the project, so all the details, including a paper about the design, can be found [here](https://github.com/dgblack/robotPhantom). A video of an early test of the breathing phantom can be found [here](https://photos.app.goo.gl/4mMbthK3jqB9catD8) (this was purely a test of the breathing mechanism without proper lungs, ribcage, etc. due to COVID-19).

To achieve anatomical accuracy, it was important to consider the material attenuation coefficients to match human soft tissue, lung, and bone under x-ray and gamma radiation. We designed a set of flexible, inflatable, anatomically realistic lungs by molding a liquid silicone elastomer onto 3D printed lungs obtained from a CT scan. These lungs are positioned inside a realistic ribcage and torso shell, which is otherwise filled with water, and actuated using a biomimetic system of negative intrapleural pressure. Initially we designed a rubber diaphragm membrane to provide the pressure changes using a linear actuator, however, after some prototyping and testing we switched to a piston mechanism. The linear actuator is position-controlled by analog output from a Raspberry-PI (actually from an MCP4725 DAC controlled by the Pi over I2C), or alternatively from an application for a Windows laptop.

#### The Assembled Phantom
![Phantom](/images/donePhantom.jpg)
![Phantom](/images/assembledPhantom.jpg)

#### Phantom Torso with Ribcage
![Phantom](/images/phantomInBox.jpg)

#### Phantom with Diaphragm Membrane, Linear Actuator, and Lungs
![Phantom](/images/basePlateAssem.jpg)

One of the first things we did was prototype (using a waterjet cutter) and test the diaphragm membrane. The CAD models for the base plate onto which the diaphragm attaches were derived from a CT scan of the phantom torso to get as accurate dimensions as possible.

#### Diaphragm Prototype
![Diaphragm Prototype](/images/prototypeDiaphragm.jpg)

As described in the [paper](https://github.com/dgblack/robotPhantom/blob/master/RobotPhantomPaper.pdf) also linked above, the diaphragm mechanism was found to be unsatisfactory, so I designed a piston mechanism. The final design is seen below. Efforts to fabricate the lungs were temporarily hampered by COVID-19, but after initial testing with balloons, the phantom works very well and breathes in a highly controllable, repeatable manner. It can achieve breathing rates up to about 25 breaths per minute at 1232ml tidal volume, and much faster at lower volumes. Any arbitrary waveform can be fed to the actuator within these limits, creating a highly flexible, realistic, and useful phantom. The lungs are now nearing completion, with 2 versions finished, and (hopefully) the final version in fabrication.

#### Early Lung Prototype in Place in Ribcage
![Installed Lung](/images/lungInstalled.jpg)

#### Breathing Mechanism on Phantom 
(with no ribcage, lungs, liver, etc. in place yet as they were temporarily inaccessible due to COVID-19)
![Breathing Mechanism](/images/physicalMechanism.jpg)

#### CAD Cross-Section of Phantom
![Breathing Mechanism CAD](/images/phantomCut.png)

#### Breathing Concept
![Breathing Concept](/images/breathingMechanism.jpg)
Respiration is achieved through incompressible-fluid (i.e. water) - mediated pressure modulation. As the piston extends, the phantom's volume effectively decreases, and the only way for this to occur is for air to flow out of the lungs. The opposite happens during inhalation.

#### 3D-Printed Lung Positive
![3D-Printed Lung Mold](/images/lungs.jpg)
The mold is printed in 2 parts due to size constraints, with no internal seam between the parts. Heat-resistant dental plaster is poured into the 3D-printed positive, and finally the high temperature vulcanization (HTV) liquid silicone rubber (LSR) is rolled onto the plaster mold and baked in an oven to set.

#### Piston and Cylinder
![Piston and Cylinder](/images/pistonCylinder.jpg)
The piston and cylinder were very carefully designed with help from the Parker O-ring Handbook to fulfill certain O-ring specifications that lead to an effective seal. These requirements were designed to be met both in the ideal situation, and in the worst case scenario of our specified manufacturer tolerances, and water and heat-induced swelling of the plastic. Material choice played an important roll in ensuring these specs could be achieved while avoiding backscattering gamma photons off metal, and minimizing piston friction.

#### Me Working on the Phantom
![Working on the Phantom](/images/installingLungs.jpg)
