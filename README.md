# VTOLproject
Contributions to the VTOL project


* Masscopter
  - By Amir, Angel, Lin, and Wilson
* Introduction
   Modern Rocket uses 2 DOF revolute joint to turn the nozzle to directly control the direction of thrust. Challenges are it has to resist a very high temperature and the joint need a large amount of energy to keep the nozzle in a specific direction. Instead, a precisely controlled off-center mass in the front of the rocket can create a torque that steers the Rocket.
   
   We aim to explore an alternative way to steer flying vehicles with underactuated controller. Taking the motivation from modern rocket control, we are going to implement such controller in a quadcopter and explore the possibilities of such control. We hope to extend such controller to steer rockets in a more cost and energy efficient manner.

   For a brief summary of our project, check out the following:
   - [[https://github.com/ajimenezUCLA/VTOLproject/blob/master/masscopter.pdf][Final Presentation]]
* Mathematical Model  
  Using Newton's fundamental law of physics, we are able to derive systems of equations that characterize the dynamics of our system. However, due to the complexity introduced by rotational acceleration, even in quaternion, no close-solution in the form of $\dot{s} = f(s)$ is analytically derived. Moreover, solving the equations in the form $f(\dot{s},s)$ numerically in Matlab yields no solutions.
  - Entire Derivation is in the Documentation

* Simulation
* Motor Exploration  
  - Simulation Demo:
  [[https://youtu.be/-pxAeULueiw][Simulink 3D Motor Demo]]
* Actual Implementation
  - video link
* List of video demos
  | Week | Link                                                                |
  |------+---------------------------------------------------------------------|
  |    1 | [[https://youtu.be/7awN_Fga4PQ][CF quadcopter First test]]                                            |
  |    2 | [[https://youtu.be/i5cuPygJWJk][Control CF2 using PS4 controller]]                                    |
  |    3 | [[https://www.youtube.com/watch?v=kcwpM1wRnxU&feature=youtu.be][3D simulation (part 1) --- quadcopter with spinning mas]]                      |
  |    4 | [[https://youtu.be/V58xpIB7BX8][Quadcopter motor test]]                                               |
  |    5 | 3D simulation [[https://www.youtube.com/watch?v=o9f2x5YUPoA&t=1s][part 2]] & [[https://www.youtube.com/watch?v=nTm2-kypBXU&feature=youtu.be][controller motor test with H-bridge]] |
  |    6 | [[https://youtu.be/SJowaesDsbo][3D printed arm test]]                                                 |
  |    7 | [[https://www.youtube.com/watch?v=24vi_tD_O_k&feature=youtu.be][Encoder of controller test]]                                          |
  |    8 | [[Controlle motor ][CF2 PWM pin control motor]] & [[https://www.youtube.com/watch?v=d_Ma3YFCfu8&feature=youtu.be][Quad-Controller all-in-one test]]         |
  |    9 | [[https://www.youtube.com/watch?v=o9f2x5YUPoA][Simulation]] & [[https://www.youtube.com/watch?v=xGmaOrivyys&feature=youtu.be][Actual Flight]]                                          |
* Scratch Board
** General Resources
  - Professor Office Hours: ? I sent an email inquiry
  - [[https://drive.google.com/drive/folders/1oTfQlVWcGNcjBcGgUbyTBhJVp0DoDn2w][google drive folder]]
  - [[https://www.overleaf.com/15319132wvnjrthtfxrp][overleaf latex]]
  - [[https://ocw.mit.edu/courses/mechanical-engineering/2-003sc-engineering-dynamics-fall-2011/newton2019s-laws-vectors-and-reference-frames/][mit dynamic course]]
  - [[http://www.es.ele.tue.nl/education/5HC99/wiki/images/4/42/RigidBodyDynamics.pdf][Inertial/Body frame, Rotation Matrix]]
** Goal / Tasks
  - WE NEED TO START ORDERING
  - ALWAYS GO TO OFFICE HOURS
** Mathematical Derivation
  - Size of the current quadcopter
  - Start having some shit on paper so we can ask more solid question during office hours
** Free Body Diagram
** Inertial Frame vs Body Frame
** Project plan
  | Milestone(s)                | Demonstration                                            |
  |-----------------------------+----------------------------------------------------------|
  | Pick our components         | Reason choosing these parts                              |
  | Hack the quadcopter         | Controll the quadcopter with Arduino code                |
  | Mathematcial Formulation    | Show our mathematical model                              |
  | Sensor Fusion               | Demonstrate angle change / vector graph                  |
  | Control circuit for motor   | Test: falling on desire side                             |
  | Develop Matlab Simulation   | Show simulation graph                                    |
  | Putting everything together | Show our modified quadcopter: video demo?                |
  | Controller Design           | Show how quadcopter reacts with different controllers    |
  | End-to-end testing          | Gather experimental results that supports our conclusion |
  | Documentation               | Document all our work                                    |

** Research Online
** Model  
   1) Describe the motion
      - assign a coordination system
   2) Apply physical law / draw free body diagram
      - F = ma
      - To draw a free body diagram
	+ draw forces in direction they act
	+ assume x and x' is positive values
	+ deduce signs from direction of arrow
	
   3) 

** Presentation Orgainzation
** Abstract
  We aim to design an underactuated controller which is essen- tially a off-center spinning mass that is able to steer flying vehicles. A quadcopter is used to demonstrate the principle of such controller. By in-depth analysis of the system dynamics and results from this project, we believe such principle can be applied to modern rockets with little modification.
** Introduction and Problem Statement
  Modern Rocket uses 2 DOF revolute joint to turn the nozzle to directly control the direction of thrust. Challenges are it has to resist a very high temperature and the joint need a large amount of energy to keep the nozzle in a specific direction. Instead, a precisely controlled off-center mass in the front of the rocket can create a torque that steers the Rocket.
  We aim to explore an alternative way to steer flying vehicles with underactuated controller. Taking the motivation from modern rocket control, we are going to implement such controller in a quadcopter to demonstrate such principle. We hope to extend such controller to steer rockets in a more cost and energy efficient manner.
** Mathematical Model and Matlab Implementation
  - All the equations we dervied
  - Implement these equations in matlab and solve 
** Simulation
  - How did we build the 3D structure
  - How did we make dynamic simulation using simulink
** Controller Design and Mounting
  - How we come up with the off-center mass design?
	+ why use the motor we chose? Light, pwm controllable speed
  - What are some challenges in designing the off center mass?
	+ maximum load
	+ the hole that goes in the motor
	+ mount it stably on the quad
** Control Circuit Design
  - The more technical part of the controller
	+ PWM
	+ SMD soldering
	+ Parallel battery source
** Quadcopter Hacking  
  - Control the thrust from computer
  - Control the output pwm signal from computer 
** Results
  - Simulation and Mathematical Model suggest it may work
  - Limitation in physical implementation may be the cause of unideal results
** Further Work
  - Hack the quadcopter: dynamically control the PWM output
  - How PWM pins affect the speed
  - Add sensor for spining off-center mass
** Conclusion
