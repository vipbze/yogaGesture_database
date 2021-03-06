# yogaGesture_database

This database contains totally 211643 data frames and 1831 posture instances.

## Subject Information

The posture database was collected from eleven subjects (ten females and one male, aged 24-34). Among the eleven subjects, subject 2, Subject 3, subject 5, and subject 6 have learned yoga to a extent, and the others have never learned yoga. Every subject was required to perform every yoga posture about 10 times with a random order and interval.

## posture Definition

18 common yoga postures were modelled as shown in the following figure. All postures are static. Based on the waist IMU coordinate relative to skeleton animation coordinate, 18 postures will be divided into 5 categories in advance. Posture 1, 4, 5, 6, 7 belong to the ”Stand” category. Posture 2, 9 belong to the ”Lean Left” category. Posture 3, 8 belong to ”Lean Right” category. Posture 10, 12, 13, 15, 17 belong to ”Lie on back” category. Posture 11, 14, 16, 18 belong to ”Lie on stomach” category.

![gesture](yoga_gestures.jpg)

## Format of Raw Data

Our sensing system includes 11 IMUs (MTw Awinda, Xsens). 11 IMUs are fixed on Head, Throax, left upper arm (LUArm), left forearm (LFArm), right upper arm (RUArm), right forearm (RFArm), waist (Waist), left thigh (LThigh), left shank (LShank), right thigh (RThigh), and right shank (RShank). The sensor may transmit the orientation data in the form of quaternion to a computer with a modifiable sampling frequency (40 Hz in this study), which could represent the orientations of IMU coordinate in the global coordinate.

The file name of raw data files is in the format of %x%num.log and %x%num.txt, where %x is the posture code name and %num is the trile num, %x%num.log is the calibration data and %x%num.txt is the measured data. The code names corresponding relation to postures are the following:

a——Stand deep breathing

bl——Left semilunar

br——Right semilunar

c——Utkatasana type

dl——Left triangle

dr——RIght triangle

el——Left tree

er——Right tree

g——Supine

hl——Left draught

hr——Right draught

i——Cobra

k——Grasshoppers

l——Lying hero

m——Half Tortoise

n—camel

o——Rabbit

p——sitting inhalation

All data of one subject is put in the same folder. 

The folder with the "nonStandard" contains the nonstandard posture data of Stand deep breathing. The file name of nonstandard data of Stand deep breathing, is in the format of %anot%num.txt and %anot%num.log, where every three files are the data of one nonstandard situation.  

Every line of a raw data file (.txt) is senser data of a sample period. Every line contains 1 int and 143 floats:

```
PacketCount	(q0	q1	q2	q3	accX	accY	accZ	gyrX	gyrY	gyrZ	magX	magY	magZ）*13
```
