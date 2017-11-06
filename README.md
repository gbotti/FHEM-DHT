# FHEM-DHT
Python Script for reading values DHT11/22 at GPIO of RaspberryPi and send them to FHEM 

### Requirements

* https://github.com/adafruit/Adafruit_Python_DHT
* https://fhem.de/

### Usage

I use this script for reading a DHT11/22 which is attached to a GPIO-Pin of the RapsberryPi and send the Values via Telnet / Netcat to a Dummy in FHEM.

### FHEM Configuration Example

    define Raspi.DHT22 dummy
    attr Raspi.DHT22 alias Temp in ServerRack
    attr Raspi.DHT22 group IT
    attr Raspi.DHT22 room Basement
    attr Raspi.DHT22 stateFormat T: Temperature H: Humidity