# cdr_erc
my topic is power electronics
//procedure for documentation
what ever they have asked just copy paste it and start answer the the questons
//go to chapter 3 
//extract requirement from chapter 3
* You must address the following minimum requirements: [size, weight, E-STOP, communications, and safe carry]
* Example, when on power electronics node, replaceable batteries and kill switch can be listed under that node as requirements
(along with numerous other requirements of that subsystem ofc)
* Understanding of key requirements was done in erc. So we have a list of requirements ready.
How we decided on them is the question to be answered
|*| requirements -take reference from arc 
|*| verification
|*| validation
power requirement of power sources (18v, 12V, 5V) to which all the components are connected in parallel.
Parallel connections are chosen to ensure that in the event of one component's failure, the remaining connections continue to function normally.
# purpose 
 //write about which battery is used for what purposes
 '12v'
normal conditions, there are two 12V LiPo batteries connected in parallel, that combine to give the 12V line
In case one of the 12V batteries stops discharging, the other 12V battery will take over and continue to supply the required current, as they are connected in parallel
 "24v"
  drive control system and linear actuator on the manipulator
  "5v"
  to provide for LoRa, encoders and relay switches
# safety mechanisms
1)Across each of the LiPo batteries, a BMS and a temperature sensor is connected, to ensure several safety features such as overcharge and reverse current protection, remote system monitoring etc
2)*kill switch 
 //physical 
 //remotely through relays which are controlled using microcontrollers.
 3)12V batteries stops discharging, the other 12V battery will take over and continue to supply the required current, as they are connected in parallel
   if the 24V battery malfunctions, the controller will ensure that the required relay switches get switched and the 12V batteries will get connected in series

# power saving 
The mobility control unit also features
two power-saving modes, the Power Saving Mode and the Ultra Power Saving Mode, which reduce the
speed of all wheels to conserve battery power. The Ultra Power Saving Mode is activated when the
primary 24V battery is depleted, and the two 12V power sources that power the manipulator are
connected in series to provide a 24V supply to the mobility motors, enabling the rover to operate for an
extended period when the primary battery is unusable.

# min req
The E-Stop button with required attributes is attached to the rover and tested under emergency situations as mentioned such as sudden mechanical accidents etc.  There’s a blue light installed inside the rover which indicates the active/on status of the rover

The developed system is capable of autonomy, consisting of wireless communication with the base station, onboard power & computation devices.

# arc 2022
Battery Management System (BMS) is designed such that the battery is well guarded through a
protective plate with a sampling resistor, and a current fuse to avoid any potential
overcharge/shorting that is either temperature-related or current-related. Proper ventilation and
spacing of batteries have been taken under consideration to protect electronic components from
overheating and avoid direct contact between the power unit and other modules.
Components of the Rover that are part of power electronics:
- 6 speed control motors with a no load current of 1.12A and stall current of 30A.
- 3 speed control motor drivers with RMS current of 30A and peak current of 80A.
- Nvidia AGX orin with RMS current of 6A.
- LoRa module with rms current of 4.2mA.
- 2 Teensy microcontrollers of 100mA each.
- LiPo battery.
- Stereo camera powered by Jetson itself.
- Master controller for manipulator.
- ## power saving 
The mobility control unit also features
two power-saving modes, the Power Saving Mode and the Ultra Power Saving Mode, which reduce the
speed of all wheels to conserve battery power. The Ultra Power Saving Mode is activated when the
primary 24V battery is depleted, and the two 12V power sources that power the manipulator are
connected in series to provide a 24V supply to the mobility motors, enabling the rover to operate for an
extended period when the primary battery is unusable.
# compailace 
we have mechanism and we will do it
*
# min req 
battery and how much volt and for what

# finial document 
The power requirements of rover is met through two different voltage lines (18V,12v and 5V), to which all the components are connected in parallel.
The 18V line will be used for Motors for the drive control system,12v Linear actuator on the manipulator,Motor for controlling steering mechanism,
for Antennas 18v line is booset to 24v,for Orin 18v line is boosted to 19v.A 5V line will be used To provide power for LoRa (Long Range) module,motor Encoders and Relay switches used in the power electronics architecture.

## saftey
* To all batteries Battery Management System (BMS) is connected to ensure that the battery is protected from overcharging and from reverse currrent.
* Electrical components were arranged considering proper ventilation for heat exchange.The system is designed such that the rover can cease operations through both a physical kill switch as well as remotely through relays which are controlled using microcontrollers, in case of emergencies.
## Components of the Rover that are part of power electronics:
//Modified 
- 4 speed control motors with a no load current of 2.7Amps and stall current of 130Amps
- 4 speed control motor drivers with RMS current of 30A and peak current of 80A.
- Nvidia AGX orin processing unit with RMS current of 6A.
- LoRa module +with rms current of 4.2mA.
- 4 stm32 microcontrollers with max current with 8.4mA. 
- LiPo batteries.
- Stereo camera powered by Nvidia AGX orin.
- Master controller for manipulator.


