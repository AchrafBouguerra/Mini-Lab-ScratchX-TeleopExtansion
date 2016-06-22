# **Welcome to the Mini-Lab-ScratchX-TeleopExtansion wiki!**


#### Establish a connection with ROS :

 >If you are using the Gazeboo simulation :
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
>If you are working with the Mini-Lab Robot :
* launch The rosbridge server using the following command :
```sh
$roslaunch rosbridge_server rosbridge_websocket.launch
```
* Connect to Mini-lab using the following command :
```sh
ssh user@"IP address of your Mini-Lab"
```
 * * You will be asked to enter a password, for further information please contact support@enovarobotics.com
 
These easy steps will allow you to upload the mini-lab's extansion into scratchX  :
* go to : www.scratchx.org .
* click on " Open Extension URL "  ( Top right of the page ).
* paste the link: https://rawgit.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/master/Teleop.js "or" https://rawgit.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/master/Short%20Version.js 
* In the popup dialog box click "I understand, continue".
* Enjoy.

The extansion on ScratchX can be reached automatically as well, simply by clicking the link below :
 http://scratchx.org/?url=https://rawgit.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/master/Teleop.js 

Use the connection Block to start the connection with the robot/gazebo: (the block takes two parameters the host adress and the communication port, the full adress would be (ws://adress:port)

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot1.png)

In case of problems you can view the Log messages using the JavaScript Console (To start the console on Google chrome: ctrl+maj+j )

The extension also provide a Hat block that return true if the connection is succefully established:

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/hat.png)

(further information on how to do this: http://wiki.ros.org/Mini-Lab/Tutorials )

### Reading the robot position :
The extension provide differents reporter block to allow reading of the robot's position and orientation on a 3d coordinates system.
( All values are in meters.)

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/position.png)

### Reading Values from the laser sensor :
The extension provide all tools needed to use the laser sensor of the minilab Robot. These tools are a set of reporters blocks that allow access to these vales:

* Start/end angle of the scan [rad]

* Angular distance between measurements [rad]

* Time between measurements [seconds]

* Time between scans [seconds]

* Minimum/maximum range value [m]

* Finally the range of a specied angle [m]

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/laser.png)
![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/laser1.png)

These blocks could be used for diffrents applications like obstacle avoidance,map scaning,...

This is an example of obstacle detection:

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/expml.png)

### Streaming live video from Minilab/Gazebo :
The extension provide a block that can stream live video on a new popup window.This block uses the web_video_server package wich should be installed on your robot or your Gazebo's host computer. Instructions could be found here:

http://wiki.ros.org/web_video_server

Then you have to start the web video server using this command:
```sh
$rosrun web_video_server web_video_server
```
Once this is done you can use the block after specifing the adress of the host and the communication port.

There is also a block to set the video parametres width,height and quality (1-100).This block must be executed befor the streaming block.

After the execution of the two blocks the full adress of the video would be something like that:

>http://'adress':'port'/stream_viewer?topic=/camera/rgb/image_raw&width='specified_width'&height='specified_height'&quality='specified_quality'

This is an example of live video streaming from gazebo:

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/camra.png)

### Streaming Map Scaning from Minilab/gazebo:
The extension provide a block that can stream real time map scaning with a visualisation of the robot's position. To be able to use this block you need first to run these commands on your robot or your gazebo's host computer:

```sh
$ roslaunch minilab_launch minilab_state_publisher.launch
$ roslaunch minilab_launch gmapping.launch
```
(Further information could be found here: http://wiki.ros.org/Mini-Lab/Tutorials/Laser_mapping)

After specifing the adress and port wich by the way are the same parametres of the connection block, a popup window should appear containing a visulisation of the robot's posion and the map scaning process.

There is also a block to set the map parametres width,height and refresh rate (sec).This block must be executed befor the Map streaming block.

This is an example of live Map scaning:

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/map.png)
>There might be some Javascript related issues with the refresh function of the map's popup window , so you might need to refresh the Map streaming block manually in order to view the real time advancement of the scaning process.

### Using the Teleop with Mini-lab :
This block of extansion, called "GamePad", tests automatically if a gamePad is plugged in or not :
* If a GamePad is not connected :

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot00.png)

* If a GamePad is connected :

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot0.png)

### Moving the robot :
After setting up the connection with the robot, either the actuall Mini-lab, or the simulation on gazeboo, we use the [Enova Mini-lab extansion]
(https://github.com/TrifiAmanallah/Mini-Lab-Scratch-Extension), and the 'GamePad' extansion.
* example :

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot06.png)

### More Details about the extansion :
* This part is in charge of testing wheather the Gamepad is connected to ypur computer or not.

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot02.png)
 * This part, gives you the freedom to choose between a different variety of buttons depending on your personnal choice and the kind of controller you are using :

 ![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot03.png)
 
 ![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot05.png)
 
 * This part holds the role of showing the angle of roation used to rotate the robot : 
 
![Alternte text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/Screenshot04.png)

### All in one Example
This is an example of how to use most features of the minilab scratch extension:

> First run these commands :
```sh
$roscore
$roslaunch minilab_launch minilab_gazebo.launch
$roslaunch minilab_launch minilab_state_publisher.launch
$roslaunch minilab_launch gmapping.launch
$roslaunch rosbridge_server rosbridge_websocket.launch
$rosrun web_video_server web_video_server
```
![Alternate text](https://github.com/TrifiAmanallah/Mini-Lab-Scratch-Extension/blob/master/Screen%20shots/Screenshot%20from%202015-08-28%2012:06:18.png)

![Alternate text](https://github.com/TrifiAmanallah/Mini-Lab-Scratch-Extension/blob/master/Screen%20shots/Screenshot%20from%202015-08-28%2012:10:53.png)

![Alternate text](https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion/blob/master/ScreenShots/from%5C.png)


> Scource code of the Minilab's Sratch Extension(https://github.com/AchrafBouguerra/Mini-Lab-ScratchX-TeleopExtansion)

> Minilab Robot Tutorial  (http://wiki.ros.org/Mini-Lab)

> Enova Robotics (www.enovarobotics.eu/)

Developped by   

               - Amanallah Trifi (T.amanallah1992@gmail.com)

               - Achraf Bouguerra (ash.bouguerra@gmail.com)










