# RobotProgramming

# Update and Install Dependencies
1. ```sudo apt-get update && sudo apt-get upgrade```
2. ```sudo apt-get install ros-melodic-uol-cmp9767m-base ros-melodic-desktop```
3. run ```source /opt/ros/melodic/setup.bash``` on every terminal you want to use
4. ```sudo apt install python-pip```
5. ```pip install numpy``` to install numpy
6. ```pip install -U scikit-learn``` to install scikit-learn

roslaunch bacchus_gazebo vineyard_demo.launch world_name:=vineyard_small
If this doesn't work, make sure you check TASK 0 again... Or, just to be on the safe side, you may want to make sure that all simulator instances really have been terminated: killall -9 gzserver
```
sudo apt-get install \
    ros-melodic-opencv-apps \
    ros-melodic-topological-utils \
    ros-melodic-topological-navigation \
    ros-melodic-topological-navigation-msgs \
    ros-melodic-strands-navigation
```
# Running the Simulation
1. Create a folder (named ```mongodb```) in your user home directory. This folder will store all database files required to run the topological map.
Note: This is required only once
2. Launch the simulation setup:
   - roslaunch ```bacchus_gazebo vineyard_demo.launch world_name:=vineyard_small```
   - roslaunch ```uol_cmp9767m_tutorial topo_nav.launch```
   - rosrun ```topological_utils load_yaml_map.py $(rospack find uol_cmp9767m_tutorial)/maps/robotnavigation.yaml```
