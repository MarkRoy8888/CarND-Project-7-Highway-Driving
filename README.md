# CarND-Path-Planning-Project
Self-Driving Car Engineer Nanodegree Program


### The result
drive highway
![](img/image1)

switch lane
![](img/image2)

### Simulator.
You can download the Term3 Simulator which contains the Path Planning Project from the [releases tab (https://github.com/udacity/self-driving-car-sim/releases/tag/T3_v1.2).  

To run the simulator on Mac/Linux, first make the binary file executable with the following command:
```shell
sudo chmod u+x {simulator_file_name}
```

### Goals
In this project your goal is to safely navigate around a virtual highway with other traffic that is driving +-10 MPH of the 50 MPH speed limit. You will be provided the car's localization and sensor fusion data, there is also a sparse map list of waypoints around the highway. The car should try to go as close as possible to the 50 MPH speed limit, which means passing slower traffic when possible, note that other cars will try to change lanes too. The car should avoid hitting other cars at all cost as well as driving inside of the marked road lanes at all times, unless going from one lane to another. The car should be able to make one complete loop around the 6946m highway. Since the car is trying to go 50 MPH, it should take a little over 5 minutes to complete 1 loop. Also the car should not experience total acceleration over 10 m/s^2 and jerk that is greater than 10 m/s^3.

#### The map of the highway is in data/highway_map.txt
Each waypoint in the list contains  [x,y,s,dx,dy] values. x and y are the waypoint's map coordinate position, the s value is the distance along the road to get to that waypoint in meters, the dx and dy values define the unit normal vector pointing outward of the highway loop.

The highway's waypoints loop around so the frenet s value, distance along the road, goes from 0 to 6945.554.

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./path_planning`.

## My code

I follow the class Q&A tip to edit my code. First,I copy the code on class to start my car.
and edit fuction step by step. I am not family witg C ++, so keeping the code templete.
I made some edit as follows

1. Line 93 to 157

using sensor fusion to detect and predict other car.
Is it safe for pass car?

2. Line 158 to 175
The code decide what should I do when car is too close to me.

3. Line 178 to 204

using previous last two points as  trajectory.

4. Line 226 to 236

to conjunction three points at a far distance. It can be edit by result for taking good performance.

5. Line 256 to 276

count different portion(x,y)

## Function

1. using getXY function to let the car follow the lane.

trans to Frenet for let the car follow the lane and not to run over the lane.
trans back to Cartesian for convience to caculate

2. taking previous data to edit my car and setting situation for takeover and safe distance.
count previous path to keep the car run safe.
keep the car on the center of the lane.

3. initialization parameter

initialization parameter
Basically follow my mentor on class.
