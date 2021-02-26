## CNC-Drawing-Machine
#Abstract:
This project shows how to design and building low cost Arduino plotter machine based on the open source hardware and software. The Arduino plotter machine has been dependent on the principle of Computer Numerical Control with limited area depends on the motion X, Y and Z axes. The objectives of this project are to design the Plotter. Basically, this plotter machine uses two nema 17 stepper motors for X and Y axis movement and a servo motor to control the movement of pen attached to plotter head. these three stepper motors are controlled by CNC V3 shield for movement (X, Y and Z axes). This machine’s movement on the X axis is 300 mm and Y axis is 300 mm. Length of travel means the linear movement of stepper motors that control for X, Y and Z axes from point to another point. The left and right movement controlled by X axis stepper motor, front-back movement controlled by Y axis stepper motor and the pen is up-down that is controlled by Z axis servo motor.

#Introduction:
The world has become a high technology with a lot of things becoming smaller and thinner. The fast-growing development of technology and manufacturing, Industrial requirement such as good and high precision quality has helped in developing the CNC machine plotter all of those can be achieved through machines that can be controlled by computers such as Computer Numerical Control (CNC) machine. To implement CNC plotter machine, several concepts must be understood such as: understanding fundamentals, Machine Mechanical design, CNC machine hardware, test each one of three axis stepper motors and connecting CNC Machine with the software tools and test it, Three axes of CNC plotter machine can do movement starting with three primary axes which are X, Y and Z axis. The Z axis is being paralleled with the X-axis.We must understand fundamental of the plotter machine, Machine design by solidwork software, implementation Machine hardware and wiring connection, Development software, test each one of three axes stepper motors, finally connect machine with Universal G code sender software tools and test Machine.

#Objectives:
The objectives of this project are to design the CNC Plotter Machine and to modify open source software and hardware to control it.

![Capture1](https://user-images.githubusercontent.com/74725425/109291680-40369300-784f-11eb-9a6a-7614b414394a.PNG)

    Figure 1. flow chart to implementation CNC plotter machine.
 
#Bill of materials

2 nema 17 steppers (*)
4 8mm smooth rods (two 400mm-long and two 320mm-long)
8 LM8UU
2 20-tooth GT2 pulleys
10 F623ZZ bearings
1 micro servo SG90 (plus a 250mm cable extender)
1 Arduino UNO
1 CNCshield
2 Pololu stepsticks
1 GT2 belt ( 1.4 meters long )
2 M10 threaded rods (400mm-long each)
8 M10 nuts
8 30mm M3 screws with nuts
8 6mm M3 screws
4 16mm M3 screws with nuts
4 M3 washers
2 4mm OD, 100mm-long carbon fiber tubes
2 15mm M3 screws
1 12V 2A power supply
1 USB cable
1 felt tip pen (or many for more fun)
#MATERIAL AND METHODOLOGY OF PROJECT:                  
In this section we will learn how to build and do experimental the project, method of this project is generally a guiding principle to handle the problem. The project implementation method is discussed briefly focusing on basic components. The framework must be clear to ensure that the project runs smoothly, and project objectives are capable of success. Figure 2 shows three subsystems of this CNC plotter machine; Mechanical system design, electronics system, and computer for software tools.

![Capture3](https://user-images.githubusercontent.com/74725425/109292600-a1129b00-7850-11eb-84d7-c6f7e8763029.PNG)

#Mechanical system design
In this section of project, the structure of CNC plotter machine has been designed and modelling in solidwork software with desired dimensions and all parts of CNC machine will be achieved before implementation the hardware of actual CNC plotter machine. Before starting the design, there are many steps of criteria must be explained. Length of travel mean the linear movement of steppers motors that controls X, Y and Z axes. The left-right motion is controlled by X axis stepper motor, front-back motion controlled by Y axis
stepper motor and the pen goes up and down by Z axis stepper motor controller. Finally, the length travel of CNC plotter machine that decided as 300 mm for X axis, 300 mm for Y axis and 15 mm up-down for Z axis. Figure 3 show CNC plotter machine design and modelling by solidwork.

![Capture2](https://user-images.githubusercontent.com/74725425/109297277-c1922380-7857-11eb-9dc3-3bc65ebd471a.PNG)

   Figure 3. CNC -Drawing Machine Solidwork Design.



#Assembly:
I recommend the following building sequence:

1. Slide two LM8UU in each of the two longest smooth rods.
2. Slide the rods into the motor pieces, one on each side (leave an extra 20mm of the rods in one of the two sides protruding from the part towards the motor, this will later be used for supporting the Arduino holder).
3. Insert the M10 treaded rods so each one supports one side of the motor-supporting pieces using a nut on each side (total 8 M10 nuts).
4. Mount the nema 17 stepper motors on the two big plastic parts using 8 M3 screws (8mm long).
5. Insert 8 M3 nuts into the nut-holders in the bottom squared carriage and place it supporting the LM8UU linear bearings you inserted in the long smooth rods already installed.
6. Take the remaining (shorter) two smooth rods and insert two LM8UU linear bearings on each one of them.
7. Insert the two endY parts on each end of the pair of smooth rods. Now you have the second axis done.
8. Insert the top square carriage over the 4 linear bearings of the shorter smooth rods.
9. Insert 4 M30 30mm-long screws in the 4 central holes of the top square carriage, put the carriage upside-down carefully so the head of the screws will lay on the table and the screws will point upward.
10. Insert one F623ZZ bearing with the flange down, next an M3 washer and finally another bearing but now with the flange up) into each one of the four screws of the top square carriage.
11. Use a post-it or a similar-size piece of paper to press it against each one of the screws protruding so paper is perforated and is pressing against the top of the bearings. The goal is for this paper to hold them in place while we put the whole thing upside-down preventing the bearings to fall off.
12. Place the top carriage over the bottom carriage so the smooth rods on the top form a right angle with the bottom smooth rods.
13. Screw lightly each one of the four M3 screws and once you notice each one is attached to the nut in the bottom tear the post-it paper apart. Next finish tightening the screws and add the other 4 M3 30mm screws that do not have a bearing but add strength to the union of top and bottom parts of the carriage.
14. Place one GT2 pulley on each stepper motor but do not tighten the grub bolt yet.
15. Place a pair of F623ZZ bearings with an M3 washer in between fixed with an M3 screw in the end Y part that will support the servo part.
16. Insert the belt all along its path (the crossings of the central carriage are a bit tricky). And once pulleys are aligned with the belt tighten the grub screws on each one.
17. Use two M3 screws and two nuts to attach the servo support part and later add the microsevo using the two screws that come with it.

18. Make sure the vertical two holes in the servo support part are 4mm diameter and that the carbon fiber tubes can be inserted into them (if not, drill the holes with a 4mm drill bit). Insert both tubes from the top but only mid way. And next insert from the top the vertical carriage (the one that looks like a smiling face). Gently push it down till you can insert the remaining half of the carbon fiber tubes so they are inserted into the bottom holes of this carriage.

19. Using a couple of M3 screws and nuts fix the pen-holder part to the vertical carriage.

20. Push the Arduino holder into the protruding smooth rods on one of the stepper motor holders. Use a couple of M3 screws to attach the Arduino board to the plastic holder.

Congratulations, the mechanical assembly has been completed.

#Arduino Uno R3
Arduino Uno is microcontroller based on ATmega328P Atmel AVR family microcontroller (MCU). It is an open source software and hardware design and manufacture a single of microcontroller. It has 14 digital Input/output pins and 6 Analogue input can be sampled using on-chip ADC. By using open source can be programming Arduino Uno. It also has 6 PWM outputs multiplexed on to the digital IO pins. Figure 4 below shows the Arduino Uno R3 circuit.

![Capture4](https://user-images.githubusercontent.com/74725425/109311091-5baf9700-786b-11eb-8573-a946199ab37d.PNG)

#CNC V3 Shield with A4988 stepper Driver Module and Heatsink for Arduino
The Arduino CNC Shield makes it easy to get your CNC projects up and running in a few hours. It uses opensource computer code on Arduino to control 2 stepper motors using 2 pieces of A4988 Stepper Motor driver breakout board, with this CNC shield and Arduino Uno, can be build project including CNC routers. The purpose of this CNC shield to control on the three axes (X, Y and Z axes) of CNC plotter machine, meaning control on the stepper motors.

![Capture5](https://user-images.githubusercontent.com/74725425/109311238-90bbe980-786b-11eb-84d9-960a5ad15901.PNG)

#Stepper Motor
The digital pulse stepper can be converted into the movement of the pen with respect to the X, Y, Z axes directions. The stepper motor is a brushless motor that distributes full rotation in several equal steps [2]. The stepper motor in Fig. 6 is defined by the property of converting several drives to a specific increase in the position of the column. Each pulse moves the column through a fixed angle. This machine has used three stepper motors with a lead screw and two belts.

The output of the motor will be in the form of the rotation of the lead screw with respect to the X, Y and Z axis.

![image](https://user-images.githubusercontent.com/74725425/109311193-800b7380-786b-11eb-99f4-be683f362113.png)

#Electronics system and wiring:

![FMSTBTKINU1G315](https://user-images.githubusercontent.com/74725425/109310605-c3191700-786a-11eb-8909-d46049c0659f.png)

The wiring of the various components of electronics system is represented in the Fig.. The microcontroller of Arduino board is connected to the computer system through the USB serial port. The Stepper Motors of two axes (X, Y ) are connected with CNC shield driver board. D.C. Power supply is provided for all the components of electronics system.

On top of Arduino you insert the CNCShield board and on top of it, two of the Pololu StepStick stepper driver boards. But before inserting these two boards for axis X and Y, make sure you put three jumpers in the headers (that will later be obstructed by the Pololu carrier boards).

A three-wire cable will be coming from the servo and two four-wire cables come from the stepper motors.

Servo cable has to go to (red) +5V, (black) GND and signal (white or brown) to Digital pin 11. Servo cable is too short, so an 250mm extension cable will be needed.

Each stepper motor goes to X and Y axis four pin headers on the CNCShield.







