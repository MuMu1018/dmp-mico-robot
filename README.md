# dmp-mico-robot
Author: Mengjiao Hong

Begin date: July 6

I create this document in order to record my progress from scratch, including the problems and solutions to them. Thanks a lot for all the help come from Siddarth Jain, Mahdieh Nejati, and Professor Brenna Argall.

## Introduction
An article about DMP Paper Implementation:
http://www.cs.utexas.edu/~sniekum/classes/RLFD-F15/papers/Pastor09.pdf

## System Installation
Installing Linux (Ubuntu 16.04)

**Tips:** Do a dual boot instead of using virtualBox (I use macOS 10.12.6)

## ROS basic Tutorials
http://wiki.ros.org/ROS/Tutorials (1-12)

## DMP codes
Understanding DMP and get codes running

https://github.com/stulp/dmpbbo (C++)

https://github.com/sniekum/dmp (Python)

### For C++ code:
Download the dmpbbo package and follow the instructions in README.md

`~$ cd catkin_ws/src`

`~/catkin_ws/src$ git clone https://github.com/stulp/dmpbbo.git`

**Notes:**
to learn how to use and code
+ look at the `docs/tutorial.pdf`
+ and demos inside every module. They are well documented and can help understand.

#### Problems & Solutions:
1. No idea about how to use `sudo make install`, lack of understanding about making progress.

+ `~/catkin_ws/src$ cd dmpbbo`
+ `~/catkin_ws/src/dmpbbo$ mkdir -p build_dir`
+ `~/catkin_ws/src/dmpbbo$ cd build_dir/`
+ `~/catkin_ws/src/dmpbbo/build_dir$ cmake ..`
+ `~/catkin_ws/src/dmpbbo/build_dir$ make`
+ `~/catkin_ws/src/dmpbbo/build_dir$ sudo make install`
+ after these steps, all .exe file will be written into the `~/Desktop/dmpbbo/bin` folder

2. If run `cmake .. -DCMAKE_BUILD_TYPE=Release` as described in [INSTALL.txt](https://github.com/stulp/dmpbbo/blob/master/LICENSE.txt), it will fail and exit at 64%.

+ run `cmake ..` instead, and it can successfully 100% make.

### For Python code:
Download the dmp package and follow the instructions in README.md

Create a new folder `/dmp/scripts`, and add `dmp_client.py`. Using sample code provided [here](http://www.ros.org/wiki/dmp).

**Notes:**
+ `/scripts` folder is for Python code, while `/src` folder is for C++ code.
+ Changing parameters inside to find out how to set the values.
+ start point position `x_0`, start point velocity `x_dot_0`, goal position `goal`, ...
