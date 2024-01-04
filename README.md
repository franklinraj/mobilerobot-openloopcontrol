# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1: give from robomaster import robot to control the robot

Step2: give direction denoted by x y z directions

Step3: give the angle and speed to move the robot 

Step4: measure the path size respective to that give the command to the robot

Step5: change the colour then and there to make control easier and at last move it fully

## Program
```
from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.6, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=255,effect="on")
    
    ep_chassis.move(x=0.3, y=0, z=80, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=1.02, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

     ep_chassis.move(x=0, y=-1.45, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=-118, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")
    
    ep_chassis.move(x=-1.55, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=-48, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")

    ep_chassis.move(x=0, y=1.4, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=0,effect="on")

    ep_chassis.move(x=2, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=128,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=85, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")

    ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=102,effect="on")

    ep_chassis.move(x=0, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=153,b=102,effect="on")


    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()

```

## MobileRobot Movement Image:
![Screenshot 2024-01-04 105557](https://github.com/franklinraj/mobilerobot-openloopcontrol/assets/148993740/7bad193a-79de-4fb4-a439-3083e8beec98)
![Screenshot 2024-01-04 105614](https://github.com/franklinraj/mobilerobot-openloopcontrol/assets/148993740/fb018260-1f6c-4576-92ae-ed4397ef74c7)
![Screenshot 2024-01-04 105650](https://github.com/franklinraj/mobilerobot-openloopcontrol/assets/148993740/51d45c55-2c26-4835-9855-d87b7439743d)



## MobileRobot Movement Video:

https://youtube.com/shorts/oav2pgUNh0c?si=W-7EuS9_aH3OUtFs

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
