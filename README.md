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
power requirement of power sources (24V, 12V, 5V) to which all the components are connected in parallel.
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


