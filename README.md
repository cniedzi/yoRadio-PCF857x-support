# yoRadio-PCF857x-support

This mod enables the use of multiple buttons to handle favorite stations in yoRadio using a PCF857x expander. The favorite stations are stored in the ESP32 flash memory.
A short button press retrieves the station (if already stored), while a long press (>1 sec) saves the current station to the slot assigned to that button.

The required connections are shown in the file "PCF857x connection diagram.jpg".
IMPORTANT: It is recommended not to use the same I2C pins as for RTC to avoid any interference; this mod uses Wire1 (while the yoRadio RTC uses Wire(0)).

To install the mod, you need to:
- Replace the "player.cpp" file in the "yoradio-main\yoRadio\src\core" directory with the provided one, or
- Manually add the three required sections to the appropriate parts of your 'player.cpp' file. Each section to be added is delimited by lines: /**************** EXTENDER ****************/.

Enjoy!
