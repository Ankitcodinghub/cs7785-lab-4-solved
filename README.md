# cs7785-lab-4-solved
**TO GET THIS SOLUTION VISIT:** [CS7785 Lab 4 Solved](https://www.ankitcodinghub.com/product/cs7785-cs-me-ece-ae-bme7785-solved-4/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;115220&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS7785 Lab 4 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
1 Overview

For this lab you can develop and test your code running on your computer. However, you must run all les on-board the robot for the demonstration. To move folders from your computer to the robot, use GIT or the scp (secure copy) command. For example,

scp -r &lt;Directory on your cpu to copy&gt; burger@&lt;ip-of-burger&gt;:&lt;Directory to copy to on robot&gt;

We strongly encourage you to use all available resources to complete this assignment. This includes looking at the sample code provided with the robot, borrowing pieces of code from online tutorials, and talking to classmates.

2 Lab Instructions

Create a package called TeamName_navigate_to_goal (refer back to the ROS tutorials from Lab 1 if needed). Useful dependencies include rospy, roscpp, sensor_msgs, std_msgs, nav_msgs, and geometry_msgs. You can add as many nodes as you like. An example structure would be:

getObjectRange: This node should detect the ranges and orientation of obstacles. It should subscribe to the scan node and publish the vector pointing from the robot to the nearest point on the object.

goToGoal: This node should subscribe to the odom node which determines the robots global position from onboad sensors for you (using dead reckoning). It should also subscribe to the getObjectRange node to determine if there are any obstacles that need to be avoided.

This node should rst read in the given goal locations from the wayPoints.txt le, or you can include them in your code some other way. You should then create several controllers that drive the robot through the sequence of given goal points without colliding with unknown obstacles. To receive full credit the robot must stop for 10 seconds within a 10cm radius of the rst goal point, 15cm radius of the second goal point, and 20cm radius of the third goal point, the robot must not hit any obstacles, and the robot must reach the destination in under 2 minutes 30 seconds.

3 Possible Issues

2. The Turtlebot3 has built in odometry which you are free to use. You can access it by subscribing to the /odom topic. It relies on proper calibration beforehand which can mess up if you move the robot during its bringup. It is highly recommended to print out the robot’s estimated pose to make sure the odometry is correct and not drifting while the robot is stationary. If you nd it is messed up it can be xed by placing the robot on the oor and restarting the bringup.

4. The angular component of the odometry is represented by a quaternion which should be used appropriately.

5. If you wish to create dead reckoning position updates yourself, or augment the ones produced in the /odom topic, you can access the IMU and encoders through published topics /imu and

/sensor_state. More details can be found at http://wiki.ros.org/turtlebot3_bringup#Published_Topics.

6. There are some problems with the motor commands sent to the robot. Make sure your commands are below 0.2m/s linear and 1.5 rad/s angular.

4 Grading

Run the code onboard the robot 25%

stopped distance outside of goal in cm

Each collision with an obstacle -5%

Take more than 2 minutes, 30 seconds to reach the nal goal point -15%

Example grade:

You run all your code on the robot. Your robot reaches the rst goal point within 10cm, hits the obstacles once but makes it within 20 cm of the second goal point, and then reaches the nal goal point within 20cm. This is all done within 2 minutes, 30 seconds. Your grade would be…

5 Submission

2. Put the names of both lab partners into the header of the python script. Put your python script and any supplementary les, in a single zip le called

Lab4_LastName1_LastName2.zip and upload on Canvas under Assignments Lab 4.

3. Only one of the partners needs to upload code.
