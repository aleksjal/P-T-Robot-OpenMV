# P-T-Robot-OpenMV

Pan&amp;Tilt Robot controlled with OpenMV H7 Plus vision sensor.

![2023-04-30-15-12-27-966](https://user-images.githubusercontent.com/13249938/235376662-e3f70a7d-f41b-4c2a-b2c9-24f05bb51d57.jpg)



Hardware.

1. OpenMV Cam H7 Plus (https://openmv.io/collections/cams/products/openmv-cam-h7-plus)

2. 2 Sets Pan Tilt Servo Mount Bracket (https://www.amazon.com/Servo-Mount-Bracket-MG996R-Steering/dp/B07PQ12TXS/ref=sr_1_6?crid=3IO348ENA9XEH&keywords=pan+and+tilt&qid=1682815811&sprefix=pan+and+tilt%2Caps%2C126&sr=8-6)

3. Servo Motor MG995/M996 - 2 servos

4. Power for servos. Any battery pack, I used 4xAA inside battery box and soldered power switch on a positive wire, to manage power across projects effectively I ve used the proto-board which comes with OpenMV vision sensor and some power terminations of different types so I can easyly provide different types of projects with power source. Here I used female wires(+/GND) to male pins on power board to feed the pan and tilt servos. One blue led with 1KOm resistor indicates the power is on.
![2023-04-30-15-08-53-393](https://user-images.githubusercontent.com/13249938/235376810-33fe0e15-3777-49fc-b1e7-7084faf220ad.jpg)

5. Some wires, face or two, bolts and nuts or something else to securely mount H7 to tilt bracket...


6. (Optional) I used raspberry pi zero 2 W to run OpenMV IDE, because I needed mobility for another project, but any computer is okay. 

Building.

Assemble Pan&Tilt with servos. I used 2 sets of brackets to firmly mount mechanism to the robot chassis, I had some brackets to mount the sensor, and OpenMV CAM comes with nice acrylyc mount frame with 4 sets of M3.

![2023-04-30-15-43-59-815](https://user-images.githubusercontent.com/13249938/235377625-73eac7fb-bc0f-412d-9d25-4ec9b471efdc.jpg)


Wiring.

In a box with the OpenMV H7 sensor I ve found very usefull compact servos PCB which allows you to manage all project wirings like a charm, just apply some soldering and voila. P7,P8, one of the GND should go to OpenMV CAM P7,P8 and GND. VCC pin and second ground to my power board, servos to servo1(pan) and servo2(tilt).

![2023-04-30-15-44-11-572](https://user-images.githubusercontent.com/13249938/235377610-61f81edf-ed06-40bb-85d9-efd58e559892.jpg)


Code.

I ve used the code from SingTown OpenMV-Pan-Tilt (https://github.com/SingTown/OpenMV-Pan-Tilt/edit/master/pan-tilt/src/find_face.py) added only this line "sensor.set_hmirror(True)" to sensor init sequence, according to my sensor orientation.

Happy hacking!

[Win 20230502 07 28 25 Pro [0.00 - 33.20].webm](https://user-images.githubusercontent.com/13249938/235697957-a44045ff-6137-4472-8629-dbc6a3c65e8f.webm)
