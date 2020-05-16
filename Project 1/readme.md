# Glow Ring
## Problem Statement
Make a ring which glows when worn
## Reqiurements
* We need small items which fit in the space of a ring.
* We cannot use too many electronic items as space is limited as well as power.
## Circuit For Detection
* A capacitive touch sensor can be utilized here and placed such that whenever a finger is pushed through the sensepad senses it.
* In addition two sense pads can be used on opposite sides of the ring, so that the detection happens only when both sensepads are active.
* The IC which is one of the cheapest, and has a deep sleep feature for power saving which I could find is *AT42QT1012*.[AT42QT1012 Datasheet](https://www.mouser.in/datasheet/2/268/40001948A-1145202.pdf)
## Power Supply
Cells which are small in size are the best option and as the IC reqires around 3V, 2 button cells of 1.5V each can be used
## LED
Best option is to use one regular LED to save power and reduce complexity. But more LEDs can be used as suited to look with higher power if reqired.
## Overall Infra
Using cello tape after connecting the circuit with a steel wire as the backbone seems good. 
Using a microcontroller may increase the size too much but nevertheless, ArduinoProMini/ ATtiny can be used

