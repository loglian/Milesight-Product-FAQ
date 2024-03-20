#CT10X Smart Current Transformer FAQ
CT10X has been launched at the end of January 24. 
CT30X is expected to be released in Q2 of 24.
Version	Context
V1.0	The initial version includes a brief introduction of the product's key features and highlights, as well as a section to address frequently asked questions regarding product usage.
Brief
The main functionality of this current transformer is to detect the current status of a single live wire and report the effective ampere-hour value and cumulative ampere-hour value. By collecting this data, users can monitor the operation of the device and calculate energy consumption for better saving power in further.

##Highlights
Self-Powered Operation
Superior Accuracy with Up to 3.3kHz Frequency
Real-time Accumulated Ampere Hour Calculation
Non-invasive Installation
Irregular Current Status Alert
Compact Size for Versatile Placement
Cable-Free Design
LoRaWAN® Wireless Technology


##Appearance




##Datasheet


##FAQ
###How to use CT10X?
Here is the introduction of CT10X for your reference :  
https://youtu.be/ESbtIVR6QSo?si=juvrGnXzds522w5-
User guide of CT10X :
CT10x User Guide-V1.0.pdf

Specific instructions:
Open the current transformer to clip it around a single-phase wire. Then close the clip with a slight “click” sound to confirm a firm grip on the wire.
Note : Do not place Phase wire and Neutral wire within a single current transformer.



The deployment process is easy and non-intrusive, ensuring that the normal operation of the tested device is not affected during installation.
Additionally, we recommend that customers configure their network in advance before on-site installation to ensure smooth communication with the gateway, thus saving installation time.
Due to the special installation environment of CT10X, customers typically do not need to frequently modify device configurations. Therefore, only the Toolbox tool on the PC is supported currently. It requires connecting the device via Type-C for pre-charging and configuration.

###Does CT30X suit for three different ranges of wires?
No. In such cases, we recommend using multiple CT10X devices as a solution.

###Does CT10X be used to detect direct current (DC)?
No, CT10X can only detect alternating current (AC). Only AC can generate an alternating magnetic field, which is required for inducing current.

###What types of cables could be detected by CT10X? Is there any limitation in terms of material and size?
There are no restrictions on the material of the cable being tested. However, the cable aperture should be smaller than 16mm.

###How long the CT10X could continue working after the tested equipment is powered off?
Based on our internal test, the device could still operate for approximately 5.3 hours from full charge to shutdown.

###Comparison between the stick antenna and suction cup antenna:
Stick antenna gain : 1.8dbi - 868M  (Antenna specifications : ZCA868-0201BSM.pdf)
                                3.0dbi - 915M     (Antenna specifications : ZCA915-0201BSM.pdf)
Suction cup antenna gain : ≤1dbi
If the ELV box has a significant impact on the signal, we recommend to use the suction cup antenna.
###The compatibility for the MS platform

####Milesight Cloud：
It is planned to be compatible with V2.12.X, with an expected release date of 24.03.13.
As for the desired features, the platform will support user-defined voltage values and power factors, along with automatic calculation of energy consumption. 
Here is an illustration showcasing these functions:




####Milesight development platform : 
It is planned to be supported at the Q3/Q4 of 2024. 
Please contact with us if you have any urgent project need to support it.

###The content of uplink packet 
Please check the details of decoder :
https://github.com/Milesight-IoT/SensorDecoders/tree/main/CT_Series/CT101
The difference of CT10X and Controller in our energy monitoring solution
Traditional energy detection solutions with controllers were wired, which is directly connecting to the power meter for data collection. Controller could only collect the data the power meter provided. The current and voltage values from power meter are precise, making the controller's energy detection solution suitable for billing applications.

While for CT10X, it offers a wireless solution that focuses more on status monitoring rather than precise measurement. By monitoring the current on the live wire, it indirectly reflects the current device status—whether it is operating normally or experiencing power failure. Additionally, through high-frequency to collect current by CT10X, the detections can be used to calculate approximate energy consumption of the measured device based on the known voltage and power factors.
