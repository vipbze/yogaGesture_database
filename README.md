# yogaGesture_database
This database contains totally 211643 data frames and 1831 gesture instances.

#Subject Information
The gesture database was collected from eleven subjects (ten females and one male, aged 24-34). Among the eleven subjects, subject 2, Subject 3, subject 5, and subject 6 have learned yoga to a extent, and the others have never learned yoga. Every subject was required to perform every yoga gesture about 10 times with a random order and interval.

#Gesture Definition
18 common yoga gestures were modelled as shown in the following figure. All gestures are static. Based on the waist IMU coordinate relative to skeleton animation coordinate, 18 gestures will be divided into 5 categories in advance. Getsure 1, 4, 7, 8, 18 belong to the ”Stand” category. Gesture 2, 5 belong to the ”Lean Left” category. Gesture 3, 6 belong to ”Lean Right” category. Gesture 9, 10, 11, 14, 16 belong to ”Lie on back” category. Gesture 12, 13, 15, 17 belong to ”Lie on stomach” category.

#Format of Raw Data
Our sensing system includes 11 IMUs (MTw Awinda, Xsens). The sensor may transmit the orientation data in the form of quaternion to a computer with a modifiable sampling frequency (40 Hz in this paper), which could represent the orientations of IMU coordinate in the global coordinate.

The file name of raw data files is in the format of %no%arm.dat, where %no is the subject No and %arm is either L or R, which means left arm and right arm respectively.

Every line of a raw data file (.dat) is senser data of a sample period. Every line contains 12 floats:
