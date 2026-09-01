# Lab 1 Answers

## Recorded Measurements

1. Measured `/chatter` publication rate:
          -Approximately 1.000 Hz.
2. Measured `/practice/count` rate with `rate_hz:=5.0`:
	 - Approximately 5.000 Hz.
3. Measured `/practice/count` rate with `rate_hz:=2.0`:
	 - Approximately 2.000 Hz.k
4. Original red-box pose:
	- `0 0 1.5 0 0 0`
5. Modified red-box pose:
	- `-1 0 1.5 0 0 0`
6. Observation of simulation time while Gazebo was playing and paused:
	 - While Gazebo was playing, simulation time continuously increased. When the simulation was paused,
	   simulation time stopped advancing.

## Engineering Questions

1. In your own words, distinguish a ROS topic, service, action, and parameter. Give one appropriate use for each.
	A topic sends continuous data between nodes.  
	A service sends a request and gets a response.  
	An action runs a longer task and can give feedback.  
	A parameter stores a setting for a node.

2. Why must a newly built workspace be sourced before `ros2 run` or `ros2 launch` can find its packages?
	Sourcing lets ROS 2 find the packages and executables in the new workspace.
3. What evidence showed that Gazebo Transport and the ROS graph are separate communication systems?
	Gazebo topics are viewed with `gz topic -l`, while ROS 2 topics are viewed with `ros2 topic list`. They use separate communication systems.
4. What did the `/clock` bridge do? What happened on the ROS side when the bridge stopped?
	The bridge made Gazebo's `/clock` available as a ROS 2 topic. If the bridge stops, ROS 2 stops receiving that clock data.
5. Explain how the measured message rates changed when the launch argument changed.
	At `rate_hz:=5.0`, `/practice/count` ran at about 5 Hz.  
	At `rate_hz:=2.0`, it ran at about 2 Hz.
