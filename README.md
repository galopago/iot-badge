# IOT-BADGE

## Electronic conference badge for programming conventions, hacking events, etc.

* Open Source (designed in [KiCad](https://www.kicad.org/)), schematic files, PCB and GERBER files open, free and available
* Comfortable wearable badge, no components on the back side.
* Max size 10 x 10 cm to take advantage of cost reductions of most PCB makers.
* Can be powered by a 3.2 v LiFePO4 AAA size battery
* Compatible with TinyGS firmware for [reception of LoRa satellites](https://galopago.github.io/english/lora-satelite-ground-station/). No modifications needed!

![Finished Badge 433 Mhz version](/iot-badge-433/assets/img/finished_badge_v00_433.jpg)

Read this in other languages: [Español](/iot-badge-433/assets/markdown/README.es.md)

## Block Diagram

![](/iot-badge-433/assets/img/iot-badge-bd.png)


## Capabilities

* ESP32 module compatible with multiple programming languages/platforms: [C/C++](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/), [Arduino](https://github.com/espressif/arduino-esp32), Python (via [MicroPython](https://micropython.org/)), JavaScript (via [Espruino](https://www.espruino.com/ESP32) or [Mongoose OS](https://mongoose-os.com/)), [Rust ([via esp-rs](https://esp-rs.github.io/book/))
* 0.96" OLED display
* Infrared LED transmitter and receiver
* WiFi
* Radio transmitter and receiver module: FSK, GFSK, MSK, GMSK and LoRa!
* Onboard PCB antenna (433 Mhz and 915 Mhz versions)
* U.FL Connector for external antenna
* RGB LED
* 0.7 W speaker
* 6 buttons: 4 arranged in D-pad and 2 function buttons
* USB-C Connector


## 433 Mhz Version
Back                           | Side                                  | External Ant                          |
-------------------------------|---------------------------------------|---------------------------------------|
![](/iot-badge-433/assets/img/back.jpg)|![](/iot-badge-433/assets/img/side.jpg) |![](/iot-badge-433/assets/img/extant.jpg) |

## Schematic Diagram 433 Version

![](/iot-badge-433/assets/img/schematic_433.png)

## Pinout connections


### SSD1306 128x64 i2c OLED display

ESP32 GPIO PIN |Function
---------------|---------
4              | SDA
15             | SCL

### Ra-02 LoRa module

ESP32 GPIO PIN |Function
---------------|---------
19             | POCI
27             | PICO
5              | SCK
18             | /CS

### Speaker

ESP32 GPIO PIN |Function
---------------|---------
25             | Speaker

### Buttons ( please use internal pull-ups! )

ESP32 GPIO PIN |Function
---------------|---------
0              | Up
13             | Down
16             | Left
17             | Right
33             | B
32             | A

### RGB LED

ESP32 GPIO PIN |Function
---------------|---------
21             | Red
22             | Green
23             | Blue

### Ifrared transmitter LED

ESP32 GPIO PIN |Function
---------------|---------
2              | Infrared LED

### VS1838b INFRARED RECEIVER MODULE

ESP32 GPIO PIN |Function
---------------|---------
12             | VS1838b output

