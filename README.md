# ABB Experimental

[ROS-Industrial][] ABB experimental meta-package.  See the [ROS wiki][] page for more information.  

## Contents

This repo holds source code for all versions.


---

__Using Moveit! with Gazebo Simulator__

First bring the robot model into gazebo:
```roslaunch abb_irb120_gazebo irb120_gazebo.launch``` 

Next load the ros_control controllers, which will be used to actuate the joints of the gazebo model:
```roslaunch abb_irb120_gazebo irb120_control.launch``` 

Finally, launch moveit! and ensure that it is configured to talk to the gazebo controllers 
```roslaunch abb_irb120_moveit_config moveit_planning_execution gazebo:=true``` 


[ROS-Industrial]: http://www.ros.org/wiki/Industrial
[ROS wiki]: http://ros.org/wiki/abb_experimental
