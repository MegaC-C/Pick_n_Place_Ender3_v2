# Pick and Place Firmware for the Creality Ender 3 V2

## !!!Warning not suited for 3D printing, as some temperature safety features are disabled!!!
all of this is derived from https://github.com/mriscoc/Ender3V2S1/releases/tag/20230904 (Ender3V2-422-MM), see commits for changes done to that configuration to obtain a Pick'n'Place Ender3 v2.
##
Most important changes (permits to use Mosfets for vaccum pump or light):

-disable THERMAL_PROTECTION_HOTENDS 

-disable THERMAL_PROTECTION_BED 

-disable HOTEND_IDLE_TIMEOUT  

##
Convenient changes to simplify OpenPnP setup:

-EXTRUDE_MINTEMP       0

-DEFAULT_MAX_FEEDRATE  { 300, 300, 30, 30 }

-HOMING_FEEDRATE_MM_M  { (30 *60), (30 *60), (10 *60) }  

-Z_CLEARANCE_FOR_HOMING  10

-Z_AFTER_HOMING         0

-TEMP_SENSOR_0 998        (permits to remove the TempSensor)

-TEMP_SENSOR_BED 998      (permits to remove the TempSensor)
