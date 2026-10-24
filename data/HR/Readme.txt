This is a readme file for the dataset in archive: KocTUM_HR_data.tar.gz or KocTUM_HR_data.zip.

This set consists of data collected from 18 human-robot dyads. For each dyad, the data is recorded at 
1 kHz, smoothed with low-pass filtering at 15 Hertz cutoff frequency, and stored as a Matlab struct, 
named dyadData_x.mat, where x in [1..18]. 

The contents of each struct is as follows:

+ data.dyadId         : an integer between 1 and 18, denoting the id for the dyad
+ data.trialId        : an integer between 1 and 3, denoting the trial number (
+ data.condition      : a string denoting the condition name (CRA: constant role allocation, 
			DPRA: discrete proactive role allocation, WPRA: weighted proactive role allocation)
+ data.completionTime : the completion time of each trial 
+ data.poseTable      : pose of the table consisting of position and orientation, i.e. x_c = [x,y,theta] 	
+ data.xRobot	      : position of the robot, i.e. x_2 = [x,y]
+ data.xHuman         : position of the human, i.e. x_1 = [x,y]
+ data.proactivity    : the proactivity level of the robot
+ data.uR             : wrench applied by the robot, i.e. u_2 = [x,y]
+ data.uRDesired      : desired wrench of the robot, i.e. u^_2 = [x,y]
+ data.uH             : wrench applied by the human, i.e. u_1 = [x,y]
+ data.uHDesired      : desired wrench of the human, i.e. u^_1 = [x,y]
+ data.uErrH_y        : human's wrench error in the redundant direction

* Please cite: Alexander Moertl, Martin Lawitzky, Ayse Kucukyilmaz, 
T. Metin Sezgin, Cagatay Basdogan, and Sandra Hirche.
"The Role of Roles: Physical Cooperation between Humans and Robots".
The International Journal of Robotics Research, vol. 31, no. 13, pp. 1656-1674 (2012)