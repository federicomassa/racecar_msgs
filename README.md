# racecar_msgs
Custom messages for the racecar_2d project

# Installation

- If you have not a ROS workspace ready, create one (follow ROS tutorials)
- `cd <workspace>/src`
- `git clone https://github.com/federicomassa/racecar_msgs`
- `cd ..`
- `catkin_make`
- `catkin_make racecar_msgs_genpy`
- `catkin_make racecar_msgs_gencpp`
- `catkin_make install`

**If you want to use the message from a virtual python environment, install it there** (is there a better way?):

`cp -r <workspace>/install/lib/python2.7/dist-packages/racecar_msgs <path_to_virtual_env>/lib/python2.7/site-packages`

## Messages

- **State**

```
Header header
float32 x
float32 y
float32 theta
float32 u
float32 v
float32 s
float32 d
```

x,y,theta are in world coordinates (theta is the yaw relative to the east, positive counter clockwise); u,v are longitudinal and lateral velocities; s,d are local track coordinates with respect to a reference line (curvilinear abscissa and transversal distance)
