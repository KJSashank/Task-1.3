# Hexapod
## Sensors and Microcontrollers
* We use 18+1 IMU sensors, any IMU sensor with I2C works such as ISM330DHCX( 9 DOF preferred but due to expense, 6 DOF can be used on partially) . We use 3 IMUs on each leg of the hexapod and one approximately on the COM of hexapod. 
* Rotory encoders can be used near motors(especially on the lowest part of the leg, which maintains the angle of inclination on each leg) for more precise information.
* The ultrasonic sensors/ToF sensors for object detection can be connected to the RPi directly using the insides( bottom and top) of the hexapod, without disturbing the legs.
* An ESP 8266 for each leg which communicates to the main Micro controller which is the RPi using Wifi via MQTT.
  * We use RPi for its high computational power, and if the hexapod is further upgraded for multitasking.
  * We use ESP 8266 as it is pretty cheap, and each ESP 8266 controls a leg hence debugging is easy and RPI can give fixed commands to each ESP on moving the leg.
## Wiring
* The wires from the IMUs and rotory encoders(if any) to the ESP8266 can be wrapped around the leg of hexapod which doesnt give out lose wires on the outside, as of the ESPs they can be situated nearly in the middle of the leg so no problems occur.
* The wiring for the COM IMU is directly connected to the RPi and the powersource(Power bank) as well is directly connected to the hexapod on the top.
## Data Flow
* The IMUs, motors and rotory encoders(if any) are connected to the ESP8266 via I2C protocol where the sensors are slaves and the ESP8266 being the master.
* The ESP8266 and the RPi communicate through wifi using the MQTT protocol, which avoids entanglement of wires.
* The Ultrasonic sensors are directly connected to the RPi via I2C again and gives out instructions to the ESPs for movemets of the  leg appropriately depending on which leg to move.
## Pipeline
Position Sensors =I2C=> ESP8266s =MQTT=> RPi ----

                                                     --- =MQTT=> ESP8266s =PWM=> Motors( change orientation accordingly)
                                                  
Object/obstacle sensors and COM IMU =I2C=> RPi --
