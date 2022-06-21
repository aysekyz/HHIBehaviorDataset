# Koc University Human-Human Interaction Behaviour Dataset for Pattern Recognition

This repository contains labelled haptic interaction data collected from Human-Human dyads in a joint object manipulation scenario. We conducted an experimental study to generate data that can be used to identify human-human haptic interaction patterns and learn models for capturing salient characteristics of dyadic interactions.

In order to identify human interaction patterns, we have developed an application where two human subjects interact in a virtual environment through the haptic channel using SensAble Phantom Premium haptic devices. The application requires the subjects to coordinate their actions in order to move the rectangular object together in a 2D maze-like environment:

<img src="https://github.com/aysekyz/HHIBehaviorDataset/blob/master/media/setup.png" height="250" alt="Human-Human Interaction Scenario">

Based on our interpretations of user interactions, we identified a set of interaction patterns that were observed frequently in our dyadic object manipulation task. Regarding these patterns, we proposed a human interaction behavior taxonomy. In the proposed taxonomy, the first layer presents a very general categorization of any physical interaction involving multiple agents. In this layer, an interaction-based perspective is adopted to classify the task as being either harmonious, conflicting, or neutral. The second layer is concerned with the "intentions" of the agents. In this sense, it is not related to the resulting motion of the object itself, but is rather responsible for defining whether the agents' motion plans agree or not. Finally, the last layer describes interaction patterns that are commonly encountered in our task. The proposed technique allows the recognition of interaction behaviours, which constitute the leaves of the following taxonomy tree:

<img src="https://github.com/aysekyz/HHIBehaviorDataset/blob/master/media/taxonomy.png" alt="Taxonomy of interaction patterns in dyadic object manipulation" width= "450pt">

During the experiment, the subjects are presented with two different scenes to observe interaction patterns in both translational and rotational motion. The first scene, which will be called the straight scene from now on, depicts a horizontal path, whereas the second scene, called the bifurcated scene, presents a fork-shaped path for the users to follow. In order to elicit different interaction patterns, we presented the subjects with different manipulation scenarios, in which conflicts between partners are artificially invoked by providing each agent with different visual information about the location of the target configuration. Please click on the following visuals to get more information on the experimental scenarios in each scene:

<p>
<center>
<table>
<tr>
<td>
<figure>
<center>
 <a href="https://github.com/aysekyz/HHIBehaviorDataset/blob/master/media/Experimental_Conditions_Straight_Scene.mp4" target="_blank">
 <img width= "390pt" src="https://github.com/aysekyz/HHIBehaviorDataset/blob/master/media/straightScene.png" alt="Straight Scene Scenarios">
 <br><font size=-1><figcaption>Video 1. Experimental Scenarios in the Straight Scene</figcaption></font>
 </a>
</center>
</figure>
</td>

<td>
<figure>
<center>
 <a href="https://github.com/aysekyz/HHIBehaviorDataset/blob/master/media/Experimental_Conditions_Bifurcated_Scene.mp4" target="_blank">
 <img width= "390pt" src="https://github.com/aysekyz/HHIBehaviorDataset/blob/master/media/bifurcatedScene.png" alt="Bifurcated Scene Scenarios">
 <br><font size=-1><figcaption>Video 2. Experimental Scenarios in the Bifurcated Scene</figcaption></font>
 </a>
</center>
</figure>
</td>
</tr>
</table>
</center>

</p>

### Downloads
40 subjects (6 female and 34 male), aged between 21 and 29, all right-handed, participated in our study. The subjects were randomly divided into two groups to form dyads that should work as partners during the experiment. Hence, this dataset consists of data collected from 20 human-human dyads. For each dyad, the data is recorded at 1 kHz and stored as a Matlab struct.

<dl>
<dt>+ Raw Interaction Data </dt>
	<dd>- Readme.txt (2.33 KB) [ <a href="https://github.com/aysekyz/HHIBehaviorDataset/blob/master/data/README.txt" target="_blank">download</a> ] </dd>
    <dd>- Koc_haptic_HHI_data.zip (2.44 GB) [ <a href="https://www.dropbox.com/s/zaq3z7l609va9li/Koc_haptic_HHI_data.zip?dl=0" target="_blank">download</a> ] </dd>
<dt>+ Videos</dt>
    <dd>- Due to large data size, the videos are not available online. However, you can reconstruct the simulated trials by running <a href="https://github.com/aysekyz/HHIBehaviorDataset/blob/master/data/simulateTrials.zip">this</a> Matlab code. </dd>
    
<dt>+ Annotations 
    <dd>- annotations.mat (39 KB) [ <a href="https://www.dropbox.com/s/zaq3z7l609va9li/Koc_haptic_HHI_data.zip?dl=0" target="_blank">download</a> ]</dd>
    <dd>- columns 1 and 2: timestamps of the start and the end of the annotation</dd>
    <dd>- column 3: duration of the timestamp</dd>
    <dd>- column 4: labels C1--C6</dd>
    <dd>- column 5: the file to which the annotation is related. The index is computed using the following code (the index is the number in column 5)</dd>

```
for sc = SCENES % [1 3] straight and bifurcated
    for user = USERS % [1 3:21] -- user 2 was missing, but we still have 20 users 
        for trial = 1:TRIAL_COUNT % 10
           index = index +1;
        end
    end
end
```

<dd></dd>
</dt> 

<dt>+ Labelled Feature Sets</dt> 
	<dd>The feature sets are stored as Matlab .mat files, each of which is a 6x1 cell array. Cells 1 to 6 respectively contain instances from classes C1 to C6 as depicted in Fig. 2 above.</dd>
        <dd>- Combined and Individual Feature Sets (16.7 MB) [ <a href="https://github.com/aysekyz/HHIBehaviorDataset/blob/master/data/featureSets.zip" target="_blank">download</a> ] </dd>
</dl>
</p>

<p>
Please note that this dataset is available 
for <b>research purposes</b> only. 
If you are interested in using the dataset, please do so 
by citing the following paper:

<p>
<em>Cigil E. Madan, Ayse Kucukyilmaz, T. Metin Sezgin, and Cagatay Basdogan</em>. <strong><a href="https://nottingham-repository.worktribe.com/index.php/output/4040487/recognition-of-haptic-interaction-patterns-in-dyadic-joint-object-manipulation" target="_blank">Recognition of 
Haptic Interaction Patterns in Dyadic Joint Object Manipulation</a></strong>. IEEE Transactions on Haptics, 8, no. 1, pp.54-66, 2015.
</p>  
     		 
<p>
The experimental procedure, and the details of how data is collected can be found in the 
aforementioned paper. May you have any queries, please direct them to 
Ayse Kucukyilmaz via e-mail:ayse.kucukyilmaz@nottingham.ac.uk
</p>
