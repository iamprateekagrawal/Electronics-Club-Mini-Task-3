### Micro Mouse Maze - TechSoc Challenge
**Problem Statement:** To build an autonomous self-contained robot (micromouse) which can get to the center of a maze in the shortest possible time.

**Constraints:**
1. The cost should be minimised to be within the TechSoc budget.
2. The size of micromouse shouldn't exceed 16cm in length/width and 100cm in height.
3. It should have a sense of position.
4. Technical errors like collisions is to be taken care of.

**Steps involved:** Starting point => Sensing walls => Following algorithm => Moving with motors => Other alignments => Repeat ===> End point

**Ideation:**
1. *Sensing Device* - I choose Ultrasonic Sensors for the three sides - front, left & right.
    * It is quite simple and cheap.
    * It has an average range of 2cm to 400cm.
    * It will help in preventing collisions, track alignment and mainly to give data for direction prediction.
    * Particularly, it can take up a considerable area due to its size (Refer to [this image](https://lh3.googleusercontent.com/proxy/gITqDVEkqnUEgdMdbilWE8spWSAW0hd7HbIdfNND8J19nQKKN5ioEOP6KyrnxrZBFA2c5idda3BOi64t6KXxOg1Rfovo_-dBS3klXiVhZNg5rLBItV1Daq1eXEXzrzGlHzHXIFrO-rqkl0NlIinWWPowSuw8j3uVriGM_o6Aai4))
2. *Motors* - I choose brushed DC motors with L298N module working together.
    * The mechanism is very simple ([Quick guide](https://dronebotworkshop.com/dc-motors-l298n-h-bridge/)) and overall cost is very minimal.
    * Allows speed control and flexible with multiple mechanisms/applications as integrating it with microcontrollers will be easy
    * L298N will act as the master and instruct the motors to make the model move in any particular direction.
3. *Microcontroller* - I choose the Arduino UNO
    * Working with other devices becomes simple and model is cheaper.
    * It will work according to an algorithm to instruct L298N and move the model as required.
4. *Chassis* - I would prefer a model with circular base to make it look somewhat like spherical in shape.
    * This mainly allows easy and fast movement as circular shape helps turn and accelerate quickly.
    * We get a larger area to dump the devices.
    * Chances of toppling of model is nil.
    * Structure made of plastic will even lessen the weight and help accelerate faster.
5. *Algorithm and code* - We have got to make it with the arduino
    * Taking the data from sensors and analysing the empty directions and alignments.
    * There's two possibility - right wall or left wall following algorithms.
    * Checking for right, left and straight, we code to tend it to reach towards the end point.
6. *Power* - A 12V Battery with 1000 mAh should work according the requirement of L298N and the motors.
7. *Dimensions* - This is an important constraint.
    * Arduino is around 7X5cm which will be allowed by circular base of diameter close to 9cm.
    * Next big material will be the battery - It will be 6X4cm at max and can be adjusted at the bottom of the model.
    * The wheels can be placed within the circular base (with a cut) - will help in agility.
    * Seeing to the contraint of 16X16cm, my model (9cm dia) with will easily adjust.
8. *Other* - Rest involves positioning the devices inside it and uploading the codes.

**Comparison with the given model in the task:**
* Chassis - It is cuboidal in that model  which may reduce agility in comparison to this circular model. Additionally, the battery can be positioned at the bottom due to its weight, else it may increase chances of toppling.
* Cost - It is very high in that model as compared to this due to usage of comparatively complex devices there.
* Dimensions - It are somewhat similar in both with that model being slightly bigger in size.
* Overall - I think that model is aimed towards smarter model with more features, while this model is a simple and direct.
