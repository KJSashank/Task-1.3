# Micromouse
## Sensors
* An HC-SR04 ultrasonic sensor to detect frontal objects is best option considering its durability. There wont be much issues with the temperature as it is in the correct range of the sensor.( But if budget and weight permits it,using a GY-53 VL53L0X Laser ToF Sensor seals the deal with literally no drawbacks at all and very stable distance finder).
* The laser ToF sensors can be replaced by GP2Y0A41SK0F IR sensors for their less price and their less weight as the sides wont require long distance finding, and short distance is sufficient... but if budget permits it having the laser ToF is better.
## Microcontroller
* ESP 32 is the best choice for the micromouse as it can do all the tasks and also it is inexpensive.
## Motors
Using stepper motors can be helpful if you want an easy mount and easy movement but ESP 32 can handle complex algorithms for a faster DC motor control hence current motors are good if we can fix them properly in the mouse.
## Software and code
* The flood fill algorith is the best one for any micromouse.
* Using Eclipse instead of Arduino IDE helps in the coding part as eclipse has many features which helps in coding(user friendly) which lack in arduino IDE.
