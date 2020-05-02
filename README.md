# Raw-RSSI-Dataset-for-Indoor-Localization-Fingerprinting

This RSSI Dataset is a comprehensive set of Received Signal Strength Indicator (RSSI) readings gathered from three different types of scenarios. Three wireless technologies were used which consisted of:
 - WiFi (IEEE 802.11n 2.4GHz band)
 - Bluetooth Low Energy (BLE) and
 - Zigbee (IEEE 802.15.4)
 
 For the experimentation, the equipment utilized consisted of Raspberry Pi 3 Model Bs, Gimbal Series 10 Beacons, and Series 2 Xbees with Arduino Uno microcontrollers.
 
  <p align="center">
Equipment used in experimentation
<img src="https://github.com/pspachos/Raw-RSSI-Dataset-for-Indoor-Localization-Fingerprinting/blob/master/img/equipment.jpg">
 </p>
 
 # Experiment
A set of tests was conducted to determine the accuracy between multiple types of system designs including: Trilateration, Fingerprinting with K-Nearest Neighbor (KNN) processing, and Naive Bayes processing while using a running average filter. For the experiments all tests were done on tables which allowed tests to be simulated at a height where a user would be carrying a device in their pocket. Devices were also kept in the same orientation throughout all the tests in order to reduce the amount of error that would occur in the measuring of RSSI values. 
 
 ## Environment
Three different experimental scenarios were utilized with varing conditions inorder to determine how the proposed system will functions according to the the environmential parameters. 

Scenario 1 was a 6.0 x 5.5 m wide meeting room. The environmental area was cleared of all transmitting devices in order to create a clear testing medium where all the devices can transmit without interference. Transmitters were placed 4 m apart from one another in the shape of a triangle. Fingerprint points were taken with a 0.5 m spacing in the centre between the transmitters. This created 49 fingerprints that would comprise the database. For testing, 10 points were randomly selected.

Scenario 2 was a 5.8 x 5.3 m meeting room. This area was a high noise environment as additional transmitting devices were placed around the environment in order to create interference in the signals. There were 16 fingerprints gathered in this scenario with a larger distance selected in order to sperate the points. In this scenario 6 testing points were randomly selected to be used for comparing the algorithms.

Scenario 3 was a 10.8 x 7.3 m computer lab. This lab was a large area with a typical amount of noise occuring due to the WiFi and BLE transmitting that were in the area. The large space also allowed for signals to experience obstructions, reflections, and interference. Transmitters were placed inorder for Line-of-Sight (LoS) to be available between the transmitters to the receiver. In total, 40 fingerprints were gathered with an alternating pattern occuring between the points. Points were taken to be 1.2 m aparts one direction, and 0.6 m apart in the other. For testing 16 randomly selected points were taken. 
 
 ## Topology
 In the testing environemnt, fingerprints were gathered to be used in the creation of a database, while tests points were selected to be used against the database for the comparison. In the figures the black dots represent the location of the transmitters and the red dots represent the locations where fingerprints and tests points were gathered where appropiate. A general overview of the experimental topologies performed can be seen here:
 <p align="center">
Scenario 1
 
  Fingerprints             |  Test Points
:-------------------------:|:-------------------------:
![](https://github.com/ssadowsk/Raw-RSSI-Dataset-2/blob/master/Images/Scenario1_Fingerprints.png)  |  ![](https://github.com/ssadowsk/Raw-RSSI-Dataset-2/blob/master/Images/Scenario1_Tests.png)

  <p align="center">
  Scenario 2
 
  Fingerprints             |  Test Points
:-------------------------:|:-------------------------:
![](https://github.com/ssadowsk/Raw-RSSI-Dataset-2/blob/master/Images/Scenario2_Fingerprints.png)  |  ![](https://github.com/ssadowsk/Raw-RSSI-Dataset-2/blob/master/Images/Scenario2_Tests.png)

<p align="center">
Scenario 3
 
  Fingerprints             |  Test Points
:-------------------------:|:-------------------------:
![](https://github.com/ssadowsk/Raw-RSSI-Dataset-2/blob/master/Images/Scenario3_Fingerprints.png)  |  ![](https://github.com/ssadowsk/Raw-RSSI-Dataset-2/blob/master/Images/Scenario3_Tests.png)
  
  </p>
  
 # Related Publications
 
 To be added...
 
 # Dataset
The RSSI dataset is seperated based on the experimental scenario and furthermore on wireless technology (i.e. WiFi, BLE, and Zigbee). Each folder contains three additional folders seperating where the data was gathered (Pathloss, Database, and Tests). Pathloss contains 18 files measuring the RSSI at varying distances from the devices. The number of files located in Database and Tests varies based on the scenario.

For each technology the file name corresponds to the point as to where the data was gathered. For specific locations, the (x,y) coordinates can be seen in the appropiate .xlsx file.

For the files in the Database and Tests folders there are approximatly 300 reading. In the Pathloss folder there are a approximatly 50 only occuring from a single node. Readings appear in the format "Node *Letter*: *Value*" where:

*Letter* corresponds to the transmitter that signal was sent from, represented by 'A', 'B', or 'C'.

*Value* is the RSSI reading.
