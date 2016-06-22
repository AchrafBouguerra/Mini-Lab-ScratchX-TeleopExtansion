# Mini-Lab

The Mini-Lab is a medium sized robot that offers the best trade-off between robustness and price.
It's suitable for research, as a test-bed for the development of indoor applications and an exciting experience to visualise the autonomous navigation that can be done reling on its camera and the 2D Scanning laser.  

  - Dimension (WxLxH) :  420x350x150 mm
  - Weight :  7 kg
  - Load Capacity :  3kg
  - Speed :  1,5 m/s
  - Autonomy : 4H
  - Batteries : 12V/10Ah
  - Controller :  Intel x86
  - Operating System : Ros
> For more information about the Mini-lab and a different variety of educational, marketing, healthcare... robots, don't hesitate to  visite [ www.enovarobotics.eu ]. 
### ScratchX
ScratchX is a platform that enables people to test experimental functionality built by developers for the visual programming language Scratch.
###### What are Scratch Extensions?
Scratch extensions make it possible for Scratch to interface with external hardware and information outside of the Scratch website through new blocks. Extensions are written in JavaScript for the ScratchX project editor.


### the Mini-Lab's SratchX Extension: 

These easy steps will allow you to upload the mini-lab's extansion in to scratchX and use it :
* go to : www.scratchx.org .
* click on " Open Extension URL "  ( Top right of the page ).
* past the link: https://rawgit.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/master/Teleop.js "or" https://rawgit.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/master/Short%20Version.js 
 * In the popup dialog box click "I understand, continue".
* Last step is to simply enjoy.

The extansion on ScratchX can be reached automatically as well by clicking one of these two links :
* The long version : http://scratchx.org/?url=https://rawgit.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/master/Teleop.js 
* The short version : http://scratchx.org/?url=https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/Short%20Version.js

### About this tutorial
This tutorial will show how to use the Mini-Lab's scratch Extension either with Gazebo simulator or the actually Minilab Robot.Follow the same instructions and specify the wright adress and port.

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot1.png)


### Connect to the Minilab/Gazebo:
The extension uses  the ROS JavaScript Library (roslibjs) witch is the core JavaScript library for interacting with ROS from the browser. It uses WebSockets to connect with rosbridge and provides publishing, subscribing, service calls, actionlib, TF, URDF parsing, and other essential ROS functionality.
So to be able to use the extension you need to have the rosbridge_server package installed on your Robot or your Gazebo's host Computer.
* Start the roscore command : 
 ```sh
 $roscore 
```
* Launch the Minilab's gazebo simulation :
```sh
$roslaunch minilab_launch minilab_gazebo.launch
```
* launch The rosbridge server using the following command :
```sh
$roslaunch rosbridge_server rosbridge_websocket.launch
```

>N.B: Most of the extension's blocks wont be able to work unless the connection is succefully established.
* (further information on how to do this: http://wiki.ros.org/Mini-Lab/Tutorials )

### Using the Teleop with Mini-lab :
This block of extansion, called "GamePad", tests automatically if a gamePad is plugged in or not :
* If a GamePad is not connected :

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot00.png)

* If a GamePad is connected :

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot0.png)

### Moving the robot :
After setting up the connection with the robot, either the actuall Mini-lab, or the simulation on gazeboo, we use the [Enova Mini-lab extansion]
(https://github.com/AchrafBouguerra/Mini-Lab-Scratch-Extension), and the 'GamePad' extansion to have the robot moving.
* example :

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot06.png)

### More Details about the extansion :
* This part is in charge of testing wheather the Gamepad is connected to ypur computer or not.

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot02.png)
 * This part, gives you the freedom to choose between a different variety of buttons depending on your personnal choice and the kind of controller you are using :

 ![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot03.png)
 
 ![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot05.png)
 
 * This part holds the role of giving an ,almost, prescise counting about the rotation and direction of your robot whole pressing the controller's button :
 
![Alternte text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot04.png)

### Short version :
 You can access this extansion through the URL "https://rawgit.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/master/Short%20Version.js", copy it in ScratchX extension URL,
 where it has just the needed commands to make the Mini-lab move.
 
 ![Alternte text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot%20from%202016-06-21%2012:49:04.png)
 
 
 
 
 > For more info about the Enova MIni-Lab extension (https://github.com/TrifiAmanallah/Mini-Lab-Scratch-Extension)
 
 > For more info about the Mini-Lab using ROS  (http://wiki.ros.org/Mini-Lab)
 
 >Moved to ScratchX by Achraf Bouguerra (ash.bouguerra@gmail.com)
 
 
 
 
 
 


 













