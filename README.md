# esp8266_P1_MQTT
Reads serial data from smart meter, and post it to MQTT topic

Copied from https://github.com/neographikal/P1-Meter-ESP8266-MQTT

use https://github.com/knolleary/pubsubclient

adjust MQTT_MAX_PACKET_SIZE to 512 in pubsubclient.h

I changed the softserial to hardware serial
![Overview](https://raw.githubusercontent.com/Johnwulp/esp8266_P1_MQTT/master/overview.png)

Connector pinout. I used pin 2,3 and 5. On a 4 pin connector this is 1,2 and 4 offcourse ;-)
![Overview](https://raw.githubusercontent.com/Johnwulp/esp8266_P1_MQTT/master/connector.png)

This schema will get you started:
![Overview](https://raw.githubusercontent.com/Johnwulp/esp8266_P1_MQTT/master/schema.png)

I did not use the connector on the right, this is used for a oled screen.
I did plan to use the LED, but it isn't implemented in code right now.

Result in MQTT lens:
![MQTTLens](https://raw.githubusercontent.com/Johnwulp/esp8266_P1_MQTT/master/mqttlensresult.jpg)

Jumer needs to be connected for meters with open collector (Landis + Gyr 350, Iskra) and for meter who don't have that, leave open (Kamstrup, Kaifa).


# BOM
T1 - BC547
R1, R2 - 1K ohm
R3 - 2.2K ohm
R4 - 470 ohm
