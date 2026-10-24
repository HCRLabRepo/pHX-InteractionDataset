This is a readme file for the dataset in archive: KocTUM_HH_data.tar.gz or KocTUM_HH_data.zip.

This set consists of data collected from 6 human-robot dyads. For each dyad, the data is 
low-pass filtered, downsampled to 25Hz and aligned. Motion is estimated by a Kalman-filter 
fusioning gyro and visual tracking data.

The data is stored as a Matlab 3x4 (i.e. 3 trials x 4 segments) cells of structs, named 
dyadData_x.mat, where x in [1..6]. 

The contents of each struct is as follows:

+ dyadData.dyadId         : an integer between 1 and 6, denoting the id for the dyad
+ dyadData.trialId        : an integer between 1 and 3, denoting the trial number 
+ dyadData.segment        : an integer between 1 and 4, denoting the segment number
+ dyadData.completionTime : the completion time of each trial 
+ dyadData.poseTable      : pose of the table consisting of position and orientation, i.e. x_c = [x,y,theta] 	
+ dyadData.velTable	  : linear and angular velocity of the table i.e. xdot_2 = [vx,vy,w]
+ dyadData.u1             : wrench applied by the first human, which starts at the left seat, cf. the human's seat at HRI experiment* (i.e. u_1 = [x,y])
+ dyadData.u2             : wrench applied by the second human, which starts at the right seat, cf. the robot's seat at HRI experiment* (i.e. u_1 = [x,y])

* Please cite: Alexander Moertl, Martin Lawitzky, Ayse Kucukyilmaz, T. Metin Sezgin, 
Cagatay Basdogan, and Sandra Hirche.
"The Role of Roles: Physical Cooperation between Humans and Robots".
The International Journal of Robotics Research, vol. 31, no. 13, pp. 1656-1674 (2012)