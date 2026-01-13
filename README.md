# yoRadio-PCF857x-support

This mod enables the use of multiple buttons to handle favorite stations in yoRadio using a PCF857x expander. The favorite stations are stored in the ESP32 flash memory.
A short button press retrieves the station (if already stored), while a long press (>1 sec) saves the current station to the slot assigned to that button.

The required connections are shown in the file "PCF857x connection diagram.jpg".
<br><br>**IMPORTANT**: It is recommended not to use the same I2C pins as for RTC (if someone uses it) to avoid any interference; this mod uses Wire(1) (while the yoRadio RTC uses Wire(0)).

To install the mod, you need to:
- Replace the "player.cpp" file in the "yoradio-main\yoRadio\src\core" directory with the provided one, or
- Manually add the three required sections to the appropriate parts of your 'player.cpp' file. Each section to be added is delimited by lines: /**************** EXTENDER ****************/.

Enjoy!

***************************************************************************

Ten mod umożliwia korzystanie z wielu przycisków do obsługi ulubionych stacji w yoRadio za pomocą ekspandera PCF857x. Ulubione stacje są przechowywane w pamięci flash procesora ESP32. Krótkie naciśnięcie przycisku wywołuje stację (jeśli została wcześniej zapisana), natomiast długie naciśnięcie (>1 sek.) zapisuje aktualną stację w slocie przypisanym do danego przycisku.

Wymagane połączenia zostały przedstawione w pliku "PCF857x connection diagram.jpg".

**WAŻNE**: Zaleca się, aby nie używać tych samych pinów I2C, co dla modułu zegara RTC (jeżeli ktoś go wykorzystuje), w celu uniknięcia zakłóceń. Ten mod korzysta z magistrali Wire(1), podczas gdy RTC w yoRadio korzysta z Wire(0).

Aby zainstalować mod, należy:
- Zastąpić plik "player.cpp" w katalogu yoradio-main\yoRadio\src\core plikiem z tego repozytorium, lub
- Ręcznie dodać trzy wymagane sekcje w odpowiednich miejscach pliku "player.cpp". Każda z dodawanych sekcji jest ograniczona liniami: /**************** EXTENDER ****************/.

Miłego korzystania!
