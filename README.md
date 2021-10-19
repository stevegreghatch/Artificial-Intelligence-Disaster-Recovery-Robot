# Introduction to Artificial Intelligence - Disaster Recovery Robot - CoppeliaSim

SOLUTION

[Video Demonstration](https://www.youtube.com/watch?v=BGbjMYSzDnA&ab_channel=StevenHatch)


    Disaster Environment: 
    •  The disaster recovery environment chosen for this assignment is the aftermath of a tornado.
    •  The floor of the scene is a ground terrain object.
    •  The obstacles that have been added to the environment are debris objects and water.
          •  smaller debris = multiple cylinders to represent household items 
          •  larger debris = elongated cuboids to represent roof rafters 
          •  water = terrain object to represent potential flooding


    Improved Disaster Recover: 
    •  The robot will improve disaster recovery by its detection of heat signatures and successful navigation of the disaster site.
    •  Heat signature detection will inform rescue crews of the location of individuals or pets in need of assistance.
    •  The robot can survey the site through utilization of sensors that prevent its collision with debris and entry into water.


    Architecture: 
            •  Added Sensors
                1.	recoveryRobot_proximity_sensor_infrared
                        •	infrared proximity sensory that allows detection of objects with a heat signature
                        •	disaster recovery aid: utilized to find humans or pets in disaster zone
                2.	recoveryRobot_proximity_sensor_laser
                        •	laser proximity sensor detects water and reroutes robot from entering water
                        •	disaster recovery aid: utilized to prevent robot from becoming immobile from water
            •  Existing Sensors
                1.	recoveryRobot_proximity_sensor_ultrasonic
                        •	modification: angle has been increased to prevent wheels from getting caught on objects
                        •	ultrasonic proximity sensor prevents robot from collisions with objects
                        •	recoveryRobot_vision_sensor
                            o   child sensor that allows vision in floating view
                            

    Internal Representation of the Environment: 
      •  The robot maintains an internal representation of the environment through its use of a vision sensor, and three proximity sensors.
            •  vision sensor provides a first-person view from the robot’s perspective
            •  ultrasonic proximity sensor informs the robot of near objects and allows it to prevent collisions 
            •  infrared proximitysensor detects heat signatures
            •  laser proximity sensor notifies the robot of approaching water and reroutes the robot to avoid entry
      •  Simultaneous internal processing of these inputs creates a representation of the surroundings which is utilized to navigate the environment. 


    Reasoning, Knowledge Representation, Uncertainty, and Intelligence:
        •  Reasoning
            •  Informed action
            •  The robot can differentiate various signals (ultrasonic, infrared, and laser)
            •  Using the gathered environmental data, the robot can act to survey the disaster site without issue and identify individuals in need of rescue
        •  Knowledge Representation
            •  Visual display
            •  The robot provides a first-person point of view
            •  The robot’s knowledge of its environment is represented in a visual format which can be used by rescue crews to monitor the robot’s performance and see potentially inaccessible areas of the disaster site
        •  Uncertainty
            •  The robot proceeds with caution
            •  The robot is traversing at a slow speed and the sensor volume parameters are set to a great enough distance as to prevent the robot from taking any undesirable action
            •  These characteristics reinforce the intention of cautious exploration
        •  Intelligence
            •  To achieve its goal, the robot combines its reasoning (utilization of its sensors and action on gathered environmental data) with its representation of knowledge (visual display), allowing it to overcome its necessary uncertainty (cautious exploration) and achieve its goal (identify individuals in need)


    Further Improvements: 
        •  Ability To Swim
            •  The prototype can be further improved by granting it the ability to swim (in the event of flooding). 
            •  Detect heat signatures in water that would otherwise be unreachable. 
        •  Reinforced Learning and Advanced Search Algorithms
            •  Reinforced Learning
                •  Improvement on the robot’s decision-making and total survey time. 
                •  The robot is awarded upon completion of a disaster site survey. 
                •  It must analyze all available square footage to reach this milestone. 
                •  The robot is penalized for each second that it takes the robot to complete its survey (starting after the time in which it would take the robot to survey the site in the most optimal path). 
                •  While reinforced learning will have to be done in a simulated environment (to map out the optimal path), its effect will influence the robot’s behavior/decision-making to navigate a real disaster zone in a more optimal fashion. 
                •  Though this method, reinforced learning aims to reach the goal of finishing a complete survey in the fastest possible time.
            •  Advanced Search Algorithms
                •  Improvement of shape and pattern recognition. 
                •  Implementation of advanced search algorithms that teach the robot to recognize common shapes/patterns corresponding with individuals in need will allow for detection of individuals without a heat signature (that might have unfortunately passed away).


    Robot Code: 
        •  See above disaster recovery robot.ttt file


    Panopto Recording: 
        •  See above 'Video Demonstration' link

-------------------------------------------------------------

INTRODUCTION

Real-time search-and-rescue robots are increasingly used to supplement the efforts of the first responders in areas affected by natural disasters. They are used to spot-check the situational awareness of people in distress, survey the extent of flood or tornado damage, evaluate the number of people that had not been evacuated from their neighborhoods, clean debris, and create passable routes.

For this task, you will use the Coppelia Robotics virtual robot and its environment to demonstrate how such robots may be used in disaster recovery. Your first step is to familiarize yourself with this technology by reviewing the information in the “Coppelia Robotics Resources Page” and “CoppeliaSim User Manual” provided in the Web Links section.

For the next step, you will thoroughly describe a disaster situation similar to the ones mentioned above. Next, you will create a virtual prototype of an autonomous robotic recovery system that demonstrates goal-seeking behaviors in navigating through a predefined area. The robotic recovery system will solve a disaster recovery problem of your choice by using the Coppelia Robotics BubbleRob and its environment as the starting point of your prototyping. You will also add sensors to the robot. These sensors will collect vital information to aid in the disaster recovery effort for the scenario you described.

REQUIREMENTS

    Using the CoppeliaSim virtual robot, create a virtual prototype of an autonomous robotic recovery system that demonstrates goal-seeking behaviors in navigating through a predefined area by doing the following: 

    A.  Describe the disaster recovery environment you chose and the two obstacles you have added to the environment. 

    B.  Explain how the robot will improve disaster recovery in the environment from part A after you have added the two obstacles from part A. 

    C.  Justify the modifications you made to CoppeliaSim’s robot architecture, including two sensors you chose to add, and explain how these sensors will aid the disaster recovery effort. 

    D.  Describe how the robot maintains an internal representation of the environment. 

    E.  Explain how the robot implements the following four concepts to achieve its goal: 
            •   reasoning 
            •   knowledge representation 
            •   uncertainty 
            •   intelligence 

    F.  Explain how the prototype could be further improved, including how reinforced learning and advanced search algorithms can improve the prototype’s performance and learning. 

    G.  Submit the robot code that you created. 

    H.  Provide a Panopto video recording that describes the robot and demonstrates its functionalities to stakeholders who are nonpractitioners and include each of the following: 
            •   a statement of the disaster recovery problem 
            •   a summary of the environment and the obstacles 
            •   a summary of the robot’s goal and objectives 
            •   a description of the robot and its architecture 
            •   a demonstration of how the robot meets its disaster recovery goals 
            •   an assessment of the robot’s capabilities 
            •   an explanation of how to improve the prototype 
