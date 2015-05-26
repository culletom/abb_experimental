# ABB Experimental

[ROS-Industrial][] ABB experimental meta-package.  See the [ROS wiki][] page for more information.  

## Contents

This repo holds source code for all versions.


### Using Moveit! with Gazebo Simulator

1. Bring the robot model into gazebo and load the ros_control controllers:
   ```roslaunch abb_irb120_gazebo irb120_gazebo.launch``` 

2. Launch moveit! and ensure that it is configured to run alongside Gazebo:
```roslaunch abb_irb120_moveit_config moveit_planning_execution_gazebo``` 



**Notes:**

1. 'No p gain specified for pid' error messages which appear during gazebo startup can be ignored. These are a result of using position contollers in ROS Hydro, as discussed in [ros-industrial/universal_robot#179][].
2. More advanced users may wish to substitute the first step with seperate launch files, so as to improve modularity of the (runtime) system.

[ROS-Industrial]: http://www.ros.org/wiki/Industrial
[ROS wiki]: http://ros.org/wiki/abb_experimental
[ros-industrial/universal_robot#179]: https://github.com/ros-industrial/universal_robot/pull/179