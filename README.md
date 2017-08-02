# dmp-mico-robot
Author: Mengjiao Hong

Begin date: July 6

I create this document in order to record my progress from scratch, including the problems and solutions to them. Thanks a lot for all the help come from Siddarth Jain, Mahdieh Nejati, and Professor Brenna Argall.

## Introduction
An article about [DMP Paper Implementation](http://www.cs.utexas.edu/~sniekum/classes/RLFD-F15/papers/Pastor09.pdf)

## System Installation
Installing Linux (Ubuntu 16.04)

Tip: Do a dual boot instead of using virtualBox (I use macOS 10.12.6)

## ROS basic Tutorials
http://wiki.ros.org/ROS/Tutorials (1-12)

## DMP codes
Understanding DMP and get codes running

https://github.com/stulp/dmpbbo (C++)

https://github.com/sniekum/dmp (Python)


### For C++ code:
Download the dmpbbo package and follow the instructions in [INSTALL.txt](https://github.com/stulp/dmpbbo/blob/master/LICENSE.txt)

`~$ cd catkin_ws/src`

`~/catkin_ws/src$ git clone ...` (link of C++ code)

#### Problem 1:
No idea where to do "sudo make install", lack of understanding about making progress

+ `~/catkin_ws/src$ cd dmpbbo`

+ `~/catkin_ws/src/dmpbbo$ mkdir -p build_dir`

+ `~/catkin_ws/src/dmpbbo$ cd build_dir/`

+ `~/catkin_ws/src/dmpbbo/build_dir$ cmake ..`

+ `~/catkin_ws/src/dmpbbo/build_dir$ make`

+ `~/catkin_ws/src/dmpbbo/build_dir$ sudo make install`

After these stpes, all .exe file will be written into the /bin folder, list them with command `~/Desktop/dmpbbo/bin$ ls`

#### Problem 2:
Follow [INSTALL.txt](https://github.com/stulp/dmpbbo/blob/master/LICENSE.txt) and run `cmake .. -DCMAKE_BUILD_TYPE=Release`, it will fail and exit at 64%.

+ run `cmake ..` instead, then it can make 100% successfully.
