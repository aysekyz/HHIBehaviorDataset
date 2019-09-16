This is a readme file for the dataset in archive: Koc_haptic_HHI_data.zip.

This set consists of data collected from 20 human-human dyads.The dyad id's range from 1 to 21, where no data exists for dyad 2.

The data is stored as 10x1 Matlab cells of structs, each cell denoting a single trial performed by a dyad.
The data files are named expData_d<x>_sc<s>.mat, where x in [1..21], and s = {1,3}. 
s = 1 denotes that the data is collected in the straight scene. 
s = 3 denotes that the data is collected in the bifurcated scene.

The contents of each struct is as follows:

+ expData.dyad           : an integer between 1 and 21 -excluding 2- denoting the id for the dyad
+ expData.scene       	 : 'STRAIGHT' (i.e. straight scene) or 'BIFURCATE' (bifurcated scene)
+ expData.scenario       : scenario Id 1..4
+ expData.scenarioName   : scenario label 
			   (i.e. 'HARMONIOUS___', 'BLIND_AGENT_1', 'BLIND_AGENT_2',  
				 'FULL_CONFLICT', or'PART_CONFLICT')
+ expData.target1Pose    : center position of agent 1's target
+ expData.target2Pose    : center position of agent 2's target
+ expData.runningTime    : running time of the task in milliseconds
+ expData.totalerrorTime : time spent during collisions with the environment in milliseconds
+ expData.pose        	 : pose of the object, consisting of position and orientation, i.e. x_c = [x,z,theta]
+ expData.velocity	 : linear and angular velocity of the object
+ expData.fOnHIP1        : forces applied by the first human, who sits at the blue end
+ expData.fOnHIP2        : forces applied by the second human, who sits at the green end
+ expData.fCollision     : response forces due to collision with the environment 
+ expData.fFriction      : forces due to friction 
+ expData.HIP1Position   : position of the grasp point of the first human, who sits at the blue end 
+ expData.HIP2Position   : position of the grasp point of the second human, who sits at the green end 
+ expData.HIP1Velocity   : velocity of the grasp point of the first human, who sits at the blue end 
+ expData.HIP2Velocity   : velocity of the grasp point of the second human, who sits at the green end


* Please cite: Cigil E. Madan, Ayse Kucukyilmaz, T. Metin Sezgin, and Cagatay Basdogan.
"Recognition of Haptic Interaction Patterns in Dyadic Joint Object Manipulation". 
IEEE Transactions on Haptics, 2015. (Pre-Print)


