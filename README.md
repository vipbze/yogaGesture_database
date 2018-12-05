# yogaGesture_database

This database contains totally 211643 data frames and 1831 gesture instances.

## Subject Information

The gesture database was collected from eleven subjects (ten females and one male, aged 24-34). Among the eleven subjects, subject 2, Subject 3, subject 5, and subject 6 have learned yoga to a extent, and the others have never learned yoga. Every subject was required to perform every yoga gesture about 10 times with a random order and interval.

## Gesture Definition

18 common yoga gestures were modelled as shown in the following figure. All gestures are static. Based on the waist IMU coordinate relative to skeleton animation coordinate, 18 gestures will be divided into 5 categories in advance. Getsure 1, 4, 7, 8, 18 belong to the ”Stand” category. Gesture 2, 5 belong to the ”Lean Left” category. Gesture 3, 6 belong to ”Lean Right” category. Gesture 9, 10, 11, 14, 16 belong to ”Lie on back” category. Gesture 12, 13, 15, 17 belong to ”Lie on stomach” category.

## Format of Raw Data

Our sensing system includes 11 IMUs (MTw Awinda, Xsens). The sensor may transmit the orientation data in the form of quaternion to a computer with a modifiable sampling frequency (40 Hz in this study), which could represent the orientations of IMU coordinate in the global coordinate.

The file name of raw data files is in the format of %x%num.log and %x%num.txt, where %x is the gesture code name and %num is the trile num, %x%num.log is the calibration data and %x%num.txt is the measured data. The code names corresponding relation to gestures are the following:

a——Stand deep breathing
bl——Left semilunar
br——Right semilunar
c——Utkatasana type
dl——Left triangle
dr-RIght triangle
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

The folder with the "nonStandard" contains the nonstandard gesture data of Stand deep breathing. The file name of nonstandard data of Stand deep breathing, is in the format of %anot%num.txt and %anot%num.log, where every three files are the data of one nonstandard situation.  

Every line of a raw data file (.txt) is senser data of a sample period. Every line contains 12 floats:
