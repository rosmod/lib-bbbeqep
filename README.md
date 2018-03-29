Beaglebone Black eQEP C++ Library
=================================

eQEP (Enhanced Quadrature Encoder Pulse) library for Beaglebone Black revision C 

Install Build Tools
-------------------------

```bash
sudo apt-get install python-catkin-tools
```

Build Library:
-------------

```bash
cd
mkdir catkin_ws #if a workspace does not already exist
cd catkin_ws
git clone https://github.com/rosmod/lib-bbbeqep.git src/lib-bbbeqep
catkin build bbbeqep
```

Update Library:
-----------------

```bash
cd ~/catkin_ws
catkin clean bbbeqep
cd src/lib-bbbeqep
git pull
cd ..
catkin build bbbeqep
```


Rosmod Source Library Setup:
-------------------------------

1. In this github repo navigate to [releases](https://github.com/rosmod/lib-bbbeqep/releases), right click on `bbbeqep.zip` (not the source code zip!) and select `Copy link address'
2. In a rosmod project, drag in a new source library to the software model
3. Paste the link in the url attribute
4. Name the source library `bbbeqep`
5. Drag the library into the `set editor` of any component that uses it
6. In the forwards section of the component add `#include "bbbeqep/eqep.h`
