# ESPhome Tagreader/writer
This project is heavily based on adonno's work, check it out: https://github.com/adonno/tagreader

This version extends on the original version by allowing for more custom "tag types" (ie. file printing tags, color tags, ect). 

It is still compatible with this blueprint: https://gist.github.com/luka6000/ec6406e44de3dff082dd7e22cedcff93

# Hardware
* Wemos Lolin S3 Mini
* PN532 NFC Reader
* WS2812 LED

# Wiring
I have wired the tag reader to the S3 mini using SPI
| PN532 Pin | Lolin S3 Mini Pin | Notes                       |
|-----------|-------------------|-----------------------------|
|VCC        | VBus              | Use thick wires for this    |
| GND       | GND               |  Use thick wires for this   |
|SCK        | GPIO12            | SPI clock                   |
|MOSI       | GPIO 11           | SPI data out                |
|MISO       | GPIO 13           | SPI data in                 |
|CS/SS      | GPIO 5            | Chip select                 |  

For the LED:

| LED Pin | Lolin S3 Mini Pin | Notes                                                                                             |
|---------|-------------------|---------------------------------------------------------------------------------------------------|
|5V       | Vbus              | Can also be connected to an available VCC on the P532, the Lolin S3 mini only has one pin for 5V  |
|GNd      | GND               | Again, can be connected on an available GND on the P532, but the lolin has two pins for GND       |
| Din     | GPIO2             |                                                                                                   |

# Building
Either install ESPhome on your computer or build directly in Home Assistant's ESPhome Device Builder. Remember to modify secrets.yaml according to your network.


# Installation
You might need to hold in the "boot" button while connecting with USB to the computer for flashing. This is not necessary when doing OTA updates.





