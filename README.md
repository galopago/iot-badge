# IOT-BADGE

## Badge for hacking events, programming courses and conferences

* Comfortable wearable badge, no components on the back side.
* Max size 10 x 10 cm to take advantage of cost reductions of most PCB makers.
* Can be powered by a 3.2 v LiFePO4 AAA size battery

## Block Diagram

![](/assets/img/iot-badge-bd.png)

## Pinout


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

