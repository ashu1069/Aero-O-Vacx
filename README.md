# Aero-O-Vacx
## Design and Analysis of a vaccine carrying UAV

##### Problem Statement
The objective is to design a UAV that can be used for the transportation and distribution of vaccines in rural areas and remote locations from a central warehouse.
The constraints & challenges are as follows:
  1. It should be able to carry 10 kg of cylindrical vaccine bottles of 4 cm in diameter and 10 cm height and weight = 50 gm
  2. Flying range ~ 10km
  3. No contamination while carrying vaccines
  4. Cargo temperature should be 2-8 ° celsius to maintain the cold chain
  5. Automated loading/unloading

##### Design Approach
Our project is to design a Quadcopter that can carry vaccines with some intrinsic challenges. However, the foremost thing to do is to design our drone from scratch. 
Use of **Altair Inspire**:
Using the CAD model, we can design the final model of our UAV.  We can identyify contacts, joints of beams used adn multi-layer structure and can even simulate the moving parts. For structural analysis of the model, Altair provides analysis on stress between parts, and using simulation of UAV, we can analyze thrust produced, speed and power performance.

 - For flying range of approximately 10 kms, the power and performance analysis are optimized owing to electronics used and structural dynamics.
 - To maintain the cargo temperature between 2-8 ° celsius, inside the payload compartment, there will be a freezing mechanism using ice packs around the compartment.
 - To adjust 10 kg of payload inside a limited size of payload box, we'll be using multilayered payload box in the size order of the airframe.
 - For automated loading/unloading of payload, we need a radio-controlled mechanism

##### Airframe Material Research
1. **Carbon fiber-reinforced composites (CRFCs)**
    Uses carbon fiber as the primary structural component.
Properties:
- Light Weight: Density = 1522 kg/m^3  (with 70% fiber weight);
                Tensile strength = 3089 MPa
                Modulus of elasticity = 191 GPa
                
- Increased strength

- Conductive - advantage/disadvantage

2. **Thermoplastics such as polyester, nylon, polystyrene, etc.**

- Density = 950 kg/m^3

- Tensile strength = 31 MPa

- Modulus of elasticity = 1.86 GPa

3. **Aluminum**

- Density = 2700 kg/m^3

- Tensile strength = 90 MPa

- Modulus of elasticity = 70 GPa

**Material selection**: Finally we chose CRFCs to keep the airframe lightweight and robust. 

**Arms**: Truss arms will be used to provide structural stability and support to the motors and ESCs. They are made of carbon rods,  lightweight and structurally strong.

**Central frame**: The central frame will comprise two levels. The one on the lower side to store the LiPo battery. Batteries are generally heavy and hence will pull the Centre of gravity down and ensure stability. The payload box will be attached here.
The other will hold the Power Distribution board, with the Flight controller mounted on top. All connections will be drawn from here. A light plastic structure will be incorporated to protect the equipment.

It’s a 30-by-30 cm board to which four frame arms of length are connected.

![drone](https://user-images.githubusercontent.com/58232141/124557034-a7480200-de56-11eb-95bb-d026b5b70178.png)

###### Electronics
- FPV Camera : HD Camera (1080 pixels, 2.5 mm lens)
- GPS tracker
- BLDC brushless motor (EMAX XA2212 1400KV; Although the above table suggests using 1500-1600 KV motors, to enhance flight time and give our smaller frame size, a lower KV rating motor has been chosen; No load current at 10V=0.5A)
- ESC (30A BLDC, they are equipped with built in BECs(Battery Eliminator circuits))
- Battery (14000 mAh 6S 30C Li-Po battery)
- Power Distribution Board (MATEK XT60 PDB)
- Flight Controller (max 30A current flow, iFlight SucceX-E F4 V2.1 Flight Controller 30.5X 30.5mm Mounting F4 FC, Built-in OSD, Barometer, Current Sensor, 8MB Black Box)
- Receiver (FlySky 2.4G 6CH FS-iA6B, Receiver PPM Output With iBus Port)
- Propeller (XOAR PJG Nylon Fibre 8” x 4” Propellor. It has better strength compared to plastic and wooden propellers and is inexpensive compared to the wooden ones.)


##### Framework Design
![drone2](https://user-images.githubusercontent.com/58232141/124560907-f001ba00-de5a-11eb-8adc-dcd6decda3d0.png)

##### Contactless Payload Delivery System
1. UAV descends and using radio control the compartment opens up.
2. The payload box of vaccine is captured orthogonally and after that compartment gets closed.
3. The compartment has inbuilt freezing mechanism of icepacks around the compartment and it maintains the cold-chain.

Two U-shaped buckles will be attached to the top of the payload. The payload box will open its bottom gate. The two U-shaped buckles will then be inserted into similar shaped cavities once the UAV descends, which will lock once the buckles enter the cavity. The UAV will take off and the payload box will then close its door. 
For delivering the vaccines, the same door will open and the drone will descend and hover at negligible height and the buckles will be unlocked. The vaccines will be dropped and the UAV will once again take off and return to the base

##### CAD Model of UAV
![Screenshot 2021-07-06 134315](https://user-images.githubusercontent.com/58232141/124565933-30b00200-de60-11eb-9339-40f23a19ac7d.png)

##### Structural Analysis


https://user-images.githubusercontent.com/58232141/124570105-327bc480-de64-11eb-91d4-3445067b1942.mp4


##### Performance Analysis
- Thrust to weight ratio is 1.5
- The hover flight time is 19 minutes     
- The specific thrust is 4.5 g/W
- Electric power used is 229 W

##### USPs of the model
- Using a composite material of aluminium and highly engineered plastics that can absorb heat from the electronic usage and maintain the temperature of the drone.
- Our UAV has an inbuilt payload storage box to eliminate any risk of contamination while carrying the payload.
- Total automated loading/unloading of payload box using a radio-controlled mechanism.
- The payload compartment will open up before loading the payload, then it lowers down on the payload box and let it inside just like engulfing an object and finally closing the door using a radio control device. No human contact is involved.
- Instead of each payload box having a freezer, we’ve decided to install a freezing system in our payload compartment of the drone itself in order to maintain temperature around 2-8 degrees Celsius. 
- Our UAV weighs  ~ 15 kg, which is lightweight and easy to maintain. We have also ensured contactless delivery and transportation of the vaccines.


