# MoveIt! Tutorials

[https://ros-planning.github.io/moveit_tutorials/](https://ros-planning.github.io/moveit_tutorials/)

[Getting Started with kinetic](http://docs.ros.org/kinetic/api/moveit_tutorials/html/doc/getting_started/getting_started.html)



## Git clone 
```
git clone -b kinetic-devel https://github.com/ros-planning/moveit_tutorials.git
```

## Move Group C++ Interface
Open two shells. In the first shell start RViz and wait for everything to finish loading(In NSCL/UR5 case):

```
roslaunch ur_gazebo ur5.launch
roslaunch ur5_moveit_config ur5_moveit_planning_execution.launch sim:=true

roslaunch ur5_moveit_config moveit_rviz.launch config:=true
```

In the second shell, run the launch file:
```
roslaunch moveit_tutorials move_group_interface_tutorial.launch
```



### Directory Structure

* Each tutorial should live in its own subdirectory within the `./doc/ <>` directory.
* Add your tutorial to `index.rst` in the root directory.
* Tutorials should use the following directory structure omitting unnecessary files and subdirectories:

```
moveit_tutorials/doc/
└── <tutorial_name>/
    ├── <tutorial_name>_tutorial.rst
    ├── CMakeLists.txt
    ├── package.xml
    ├── setup.py
    ├── images/
    │   └── <tutorial_name>_<image_description>.png
    ├── include/
    │   └── <tutorial_name>/
    │       └── <include_header>.h                      # Any custom C++ library header files
    ├── launch/
    │   └── <tutorial_name>_tutorial.launch
    ├── src/
    │   ├── <tutorial_name>_tutorial.cpp                # Main C++ executable
    │   ├── <include_source>.cpp                        # Custom C++ library source files
    │   └── <tutorial_name>/
    │       ├── __init__.py
    │       ├── <tutorial_name>_tutorial.py             # Main Python executable
    │       └── <python_library>.py                     # Custom Python libraries
    └── test/                                           # Ideally tutorials have their own integration tests
        ├── <tutorial_name>_tutorial.test               # Launch file for tests
        ├── <tutorial_name>_tutorial_test.py            # Python tests for tutorial
        └── <tutorial_name>_tutorial_test.cpp           # C++ tests for tutorial
```
