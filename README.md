# Monte Carlo Localisation
Exploration of Monte Carlo Localisation algorithm.

This project was implemented with the powerful CoppeliaSim (Edu version) simulator for design & analysis of robots. 
Scripting was done in Lua, a high-level programming language, with great API support by CoppeliaSim.

## Desired outcome
The robot will navigate throughout the map utilising waypoint navigation. This will be achieved using the Monte Carlo Localisation algorithm with the use of a depth sensor. By predicting its own pose, the robot will adapt and tweak its motion to achieve precision.

## Implementation
1) Robot will generate a pool of 100 possible future poses after it completes its motion. This is done based purely on odometry and gaussian noise
3) Next, the robot will make a measurement with the sonar sensor, calculating likelihoods for each generated pose.
4) Normalisation is then done to equalise the weights among all the poses.
5) By resampling, the poses are then filtered down. The robot then determines the pose that it will most likely have.
6) The robot will then calculate the amount it should move in the x and y direction, as well as amount of rotation it should make, relative to the pose with the highest probability.

## Video Demonstration


https://user-images.githubusercontent.com/31171083/160496707-3bc2e8bb-aef5-41bd-b90b-9feaca5e4160.mp4

