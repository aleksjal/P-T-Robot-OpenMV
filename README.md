# P-T-Robot-OpenMV

Pan&amp;Tilt Robot controlled with OpenMV H7 Plus vision sensor.

![2023-04-30-15-12-27-966](https://user-images.githubusercontent.com/13249938/235376662-e3f70a7d-f41b-4c2a-b2c9-24f05bb51d57.jpg)



Hardware.

1. OpenMV Cam H7 Plus (https://openmv.io/collections/cams/products/openmv-cam-h7-plus)

2. 2 Sets Pan Tilt Servo Mount Bracket (https://www.amazon.com/Servo-Mount-Bracket-MG996R-Steering/dp/B07PQ12TXS/ref=sr_1_6?crid=3IO348ENA9XEH&keywords=pan+and+tilt&qid=1682815811&sprefix=pan+and+tilt%2Caps%2C126&sr=8-6)

3. Servo Motor MG995/M996 - 2 servos

4. Power for servos. Any battery pack, I used 4xAA inside battery box and soldered power switch on a positive wire, to manage power across projects I used the proto-board which comes with OpenMV vision sensor and some power output terminations of different types so I can easyly provide different types of projects with power source.  
![2023-04-30-15-08-53-393](https://user-images.githubusercontent.com/13249938/235376810-33fe0e15-3777-49fc-b1e7-7084faf220ad.jpg)

5. Some wires, face or two, bolts and nuts or something else to securely mount H7 to tilt bracket...
...optional

6. I used raspberry pi zero 2 W to run OpenMV IDE, because I needed mobility for another project, but any computer is okay. 

Building.

Assemble Pan&Tilt with servos. I used 2 sets of brackets to firmly mount mechanism to the robot chassis, I had some brackets to mount the sensor, and in the box you ll find nice acrylyc mount frame with 4 sets of M3.

![mechanism]![2023-04-30-15-16-35-196](https://user-images.githubusercontent.com/13249938/235376718-805e2c61-2732-4ce9-9760-d3fa086c617b.jpg)

Wiring.

In a box with the OpenMV H7 sensor I ve found very usefull compact servos PCB which allows you to manage all project wirings like a charm, just apply some soldering and voila.

![servo-board]![2023-04-30-15-10-40-519](https://user-images.githubusercontent.com/13249938/235376739-058c667b-a547-49af-81e1-630d9c8e5411.jpg)

Code.

I am totally new to Python and I ve used code from SingTown OpenMV-Pan-Tilt (https://github.com/SingTown/OpenMV-Pan-Tilt/edit/master/pan-tilt/src/find_face.py) with only one change. 
I ve added this line "sensor.set_hmirror(True)" to sensor init sequence, according to my sensor orientation.

