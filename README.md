# ril_mm_objects
 
## Overview
This is a package for spawning objects in Gazebo 




## Guide

- For spawn objects 
```
$ cd ~/catkin_ws/src && git clone https://github.com/Beom0611/ril_mm_objects.git
$ cd ~/catkin_ws && catkin_make
```

- Spawning Objects in gazebo 
### please add following lines in {your gazebo_world.launch}
```  
<node name="{node name}" pkg="gazebo_ros" type="spawn_model" args="-file $(find {folder name})/{urdf directory}/{urdf file name.urdf} -urdf -model {model name} -x 0 -y 0 -z 1" />
```
- Examples  
``` 
<node name="spawn_banana_urdf" pkg="gazebo_ros" type="spawn_model" args="-file $(find ril_mm_objects)/urdf/banana.urdf -urdf -model banana -x 5 -y 0.5 -z 1.1" />
```
- Launch    
```
$ roslaunch {your package nmae} {your gazebo_world.launch} 

```


## Description    

<img width="500" height="300" src="file:///home/park/spawn_objects.png"  alt="Screenshot" title="Screenshot">
