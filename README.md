# hyq2max_description
Simplified descritption files of the HyQ2Max robot, from IIT, to use in the ROS 2 Galactic. 

To control the joints postion is necessary use the package <a href="https://github.com/AureoGD/hyq2max_ros2_impedance_controller.git" target="_blank"> hyq2max_ros2_impedance_controller</a> and <a href="https://github.com/AureoGD/hyq2max_interfaces.git" target="_blank"> hyq2max_interfaces</a>. 

Also, it is necessary the <a href="https://github.com/ros-controls/ros2_control.git" target="_blank"> ros2_control</a>, <a href="https://github.com/ros-controls/ros2_controllers.git" target="_blank"> ros2_controller</a>, <a href="https://github.com/ros-simulation/gazebo_ros2_control.git" target="_blank"> gazebo_ros2_control</a>.

To change the joints references it is necessary to publish the new references at "/hyq2max_ros2_impedance_controller/commands" topic, using the following format:

ros2 topic pub /hyq2max_ros2_impedance_controller/commands hyq2max_interfaces/msg/JointsReferences '{q_r: [-0.05, 0.45, -1.18, -0.05, 0.45, -1.18, -0.05, -0.45, -1.18, -0.05, -0.45, 1.18], qd_r:[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]}'

All the robot states are avalible in the topic "/hyq2max_ros2_impedance_controller/robot_states".
