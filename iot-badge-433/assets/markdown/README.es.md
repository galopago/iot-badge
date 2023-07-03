# IOT-BADGE

## Gafete electronico para conferencias de programacion, eventos de hackers, etc.

* Codigo abierto (disenado en [KiCad](https://www.kicad.org/)), diagramas esquematicos, circuito impreso y archivos GERBER abiertos, gratuitos y disponibles!
* Comodo para usar, no hay componentes en la cara de atras del circuito impreso.
* Tamaño maximo 10 x 10 cm para lograr costos economicos en la fabricacion del circuito impreso que ofrecen la mayoria de fabricantes para tarjetas de dimensiones iguales o menores a esta.
* Puede ser alimentado mediante una bateria AAA LiFePO4 de 3.2 v.
* Compatible con el firmware de TinyGS [para reception de satelites LoRa ](https://galopago.github.io/espanol/lora-satelite-estacion-terrena/). No se requiere ninguna modificacion!

![Finished Badge](/assets/img/finished_badge_v00.jpg)

Lea esto en otros idiomas: [English](../../README.md)

## Diagrama de bloques

![](/assets/img/iot-badge-bd.png)


## Perifericos disponibles

* Modulo ESP32 compatible con multiples lenguajes/plataformas de programacion: [C/C++](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/), [Arduino](https://github.com/espressif/arduino-esp32), Python (via [MicroPython](https://micropython.org/)), JavaScript (via [Espruino](https://www.espruino.com/ESP32) or [Mongoose OS](https://mongoose-os.com/)), [Rust ([via esp-rs](https://esp-rs.github.io/book/))
* Pantalla OLED de 0.96"
* LED transmisor infrarojo y receptor.
* WiFi
* Radio transmisor de 433 Mhz (incluyendo LoRa) conectado a una antena interna formada en el circuito impreso!
* Conector U.FL para antena externa de 433 Mhz.
* LED RGB
* Bocina de 0.7 W
* 6 butone: 4 configurados como cruceta y 2 botones de funcion adicional
* Conector USB-C

Detras                         | Lateral                               | Antena Externa                        |
-------------------------------|---------------------------------------|---------------------------------------|
![](/assets/img/back.jpg)|![](/assets/img/side.jpg) |![](/assets/img/extant.jpg) |

## Diagrama Esquematico

![](/assets/img/schematic.png)

## Conexiones de pines entre los perifericos y el modulo ESP32


### Pantalla OLED i2c SSD1306 128x64

ESP32 GPIO PIN |Funcion
---------------|---------
4              | SDA
15             | SCL

### modulo LoRa Ra-02

ESP32 GPIO PIN |Funcion
---------------|---------
19             | POCI
27             | PICO
5              | SCK
18             | /CS

### Bocina

ESP32 GPIO PIN |Funcion
---------------|---------
25             | Bocina

### Butones ( hay que usar internos! )

ESP32 GPIO PIN |Funcion
---------------|---------
0              | Arriba
13             | Abajo
16             | Izquierda
17             | Derecha
33             | B
32             | A

### LED RGB

ESP32 GPIO PIN |Funcion
---------------|---------
21             | Rojo
22             | Verde
23             | Azul

### LED Infrarojo transmisor

ESP32 GPIO PIN |Funcion
---------------|---------
2              | LED Infrarojo

### MODULO RECEPTOR INFRAROJO VS1838b

ESP32 GPIO PIN |Funcion
---------------|---------
12             | salida del VS1838b

