# ROS
PythonForRobotics_Unit6_MicroProject
from robot_control_class import RobotControl
robotcontrol = RobotControl()
a = robotcontrol.get_laser(360)

if a > 1 :
    robotcontrol.move_straight_time("forward", 0.3, 14)
    robotcontrol.turn("clockwise", 0.3,4)
    print("The laser value received was: ", a)
    robotcontrol.move_straight_time("forward", 0.3, 12)
    robotcontrol.turn("clockwise", 0.3,4)

    robotcontrol.move_straight_time("forward", 0.3, 10)
    robotcontrol.turn("counter-clockwise", 0.3,5)

    robotcontrol.move_straight_time("forward", 0.3, 18)

else :

    robotcontrol.stop()
    print("The laser value received was: ", a)
    
    //See Video on https://youtu.be/UsAK3x8cztE//
