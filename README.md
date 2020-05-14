# ESP32_WebRadio
An Internet web radio based to ESP32

ESP32 connect to the Internet via WiFI (support PSK/PSK2), fetching MP3/AAC audio stream from your favourite webradio (mine is Dance Wave!). Then decode MP3 and send via I2S to DAC. The DAC simply output audio.

![ESP32 WebRadio](https://raw.githubusercontent.com/michelep/ESP32_WebRadio/master/images/esp32_webradio_front.jpg)

![ESP32 WebRadio inside](https://raw.githubusercontent.com/michelep/ESP32_WebRadio/master/images/esp32_webradio_inside.jpg)

## Configuration

Edit data/config.json file with your wifi ESSID and password. Fill data/streams.json with your favourites streams. Then burn the whole data directory into SPIFFS partition. Other stuff can be edited via web interface, available after successfull contection to the net. 

## Bill of materials

- DOIT ESP32 WebKit v1 (or other suitable ESP32 board...) ![AliExpress](https://it.aliexpress.com/item/4000141080480.html)
- CJMCU 5102 DAC ![AliExpress](https://it.aliexpress.com/item/33023894667.html)
- PCD8544 LCD Display (aka NOKIA 5110 display) module ![AliExpress](https://it.aliexpress.com/item/32959195226.html)
- One or more NeoPixel, but they are not mandatory ;-)
- 3 x 10KOhm 1/8W resistors
- 330Ohm 1/8W resistor
- 810Ohm 1/8 W resistor, only if you want to add one or more NeoPixels
- 3 push buttons ![AliExpress](https://it.aliexpress.com/item/32995191209.html)

## Schematic
![Schematic](https://raw.githubusercontent.com/michelep/ESP32_WebRadio/master/images/schematic.png)

## ChangeLog

0.0.1 - 08.05.2020 
  - First public release

0.0.2 - 09.05.2020
  - Added streams.json with lists of stream URL to be played
  - Some minon bugs fixed

0.0.3 - 14.05.2020
  - Some design changes, like 3 mechanical buttons (but you can use capacitive ones, if you want)
  - Streams list also on webpage, with the ability to play each with a click
  - Display graphic improvementes
  - Lots of new features and bugs fixed
  - Other minor changes

## Other resources

Start with ESP32 pinouts from here: https://randomnerdtutorials.com/esp32-pinout-reference-gpios/
Needs the great work from Wolle for MP3 stream decoding and I2S interface: https://github.com/schreibfaul1/ESP32-audioI2S
A great tutorial for Nokia 5110 LCD displays is there: https://lastminuteengineers.com/nokia-5110-lcd-arduino-tutorial/

## Contributions

This work is free and far to be perfect nor complete. Contributions and PR are welcome and strongly encouraged!
