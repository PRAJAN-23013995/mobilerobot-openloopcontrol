# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:
Import robot and camera from robomaster, and import time.

Step2:
Create the necessary objects from the imported modules.

Step3:
Start the video stream.

Step4:
Move the robot step by step to reach the initial direction by using variables x,y and z, where x represents front and back direction , y represents left and right direction and z represents rotation of axis in clockwise and anticlockwise diredtion.

Step5:
Stop the video stream and end the program.

## Program
Developed by: PRAJAN P
Register no: 212223240121
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

    ep_chassis.move(x=2.5, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=0,effect="on")

    ep_chassis.move(x=0.5, y=0, z=80, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")

    ep_chassis.move(x=1, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=0,effect="on")

    ep_chassis.move(x=0, y=-1.7, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=255,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=50, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=102,g=0,b=102,effect="on")

    ep_chassis.move(x=1.4, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=204,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=55, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=153,b=255,effect="on")

    ep_chassis.move(x=1.5, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=102,effect="on")
    
    ep_chassis.move(x=0, y=-2.15, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=102,b=204,effect="on")

    ep_chassis.move(x=0, y=0, z=175, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=102,effect="on")

    ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=128,b=128,effect="on")
    
    ep_chassis.move(x=0, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=100,b=0,effect="on")


    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```

## MobileRobot Movement Image:

![robomaster](https://github.com/PRAJAN-23013995/mobilerobot-openloopcontrol/assets/150313345/9d03315b-554e-48bf-8054-b7b51e52fd83)

![robot](https://github.com/PRAJAN-23013995/mobilerobot-openloopcontrol/assets/150313345/4947bdc7-1bab-4e77-a1d6-74e200ada2b8)

![68747470733a2f2f696d672e796f75747562652e636f6d2f76692f717841584b5779554e616f2f302e6a7067](https://github.com/PRAJAN-23013995/mobilerobot-openloopcontrol/assets/150313345/288a4cd1-eec9-47e5-a7da-23fb25414719)

## MobileRobot Movement Video:

https://youtu.be/rXrahsv0CPQ

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
