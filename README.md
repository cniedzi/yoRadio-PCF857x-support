# yoRadio-PCF857x-support

This mod enables the use of multiple buttons to handle favorite stations in yoRadio using a PCF857x expander. The favorite stations are stored in the ESP32 flash memory.
A short button press retrieves the station (if already stored), while a long press (>1 sec) saves the current station to the slot assigned to that button.

The required connections are shown in the file "PCF857x connection diagram.jpg".
<br><br>**IMPORTANT**:
- If the project uses an external RTC, the I2C's SDA and SCL pins for both the expander and the RTC can be the same (recommended).
- If an I2C display is used in addition to the RTC, then the SDA and SCL pins for the expander must be the same as those used for the RTC!

Installation:
1. In Arduino IDE/Pioarduino add Adafruit PCF8574 library (https://github.com/adafruit/Adafruit_PCF8574)
2. Replace the "player.cpp" file in the "yoradio-main\yoRadio\src\core" directory with the provided one, or manually add the three required sections to the appropriate parts of your "player.cpp" file. Each section to be added is delimited by lines: /**************** EXTENDER ****************/ in the provided "player.cpp" file.
3. In the above mentioned file "player.cpp" set the expander parameters according to your configuration (section: EXPANDER CONFIGURATION)
4. Build & upload

Enjoy!

***************************************************************************

Ten mod umożliwia korzystanie z wielu przycisków do obsługi ulubionych stacji w yoRadio za pomocą ekspandera PCF857x. Ulubione stacje są przechowywane w pamięci flash procesora ESP32. Krótkie naciśnięcie przycisku wywołuje stację (jeśli została wcześniej zapisana), natomiast długie naciśnięcie (>1 sek.) zapisuje aktualną stację w slocie przypisanym do danego przycisku.

Wymagane połączenia zostały przedstawione w pliku "PCF857x connection diagram.jpg".

**WAŻNE**
- Jeżeli projekt wykorzystuje zewnętrzny RTC, piny I2C SDA i SCL ekspandera oraz RTC mogą być takie same (zalecane).
- Jeżeli oprócz RTC wykorzystywany jest wyświetlacz I2C, wtedy dla ekspandera należy wybrać piny SDA i SCL takie jak dla RTC!

Instalacja:
1. W Arduino IDE/Pioarduino dodaj bibliotekę Adafruit PCF8574 (https://github.com/adafruit/Adafruit_PCF8574)
2. Zastąp plik "player.cpp" w katalogu yoradio-main\yoRadio\src\core plikiem z tego repozytorium, lub ręcznie dodaj trzy wymagane sekcje w odpowiednich miejscach pliku "player.cpp". Każda z ww. sekcji jest ograniczona liniami: /**************** EXTENDER ****************/ w dostarczonym pliku "player.cpp".
3. W wyżej wymienionym pliku „player.cpp” ustaw parametry ekspandera zgodnie ze swoją konfiguracją (sekcja: EXPANDER CONFIGURATION).
4. Skompiluj i wgraj (Build & upload)

Miłego korzystania!
