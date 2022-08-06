# DTUsimMI
DTU simulator for Hoymiles MI Microinverter

This software is a QUICK&DIRTY SW for debugging/controlling the MI inverter, tested with MI1500 and 3 PV's.
Based on the orig. SW from Hubi(https://github.com/hm-soft/Hoymiles-DTU-Simulation).
https://www.mikrocontroller.net/topic/525778

Do not expect any quality!
As far as you know what you are doing, you can do everything with this sw.

Runs on ESP8266: wifi, mqtt, on serial monitor and on web site, shows all data.
Runs on Arduino: no wifi, serial monitor shows all data.
arduino-ide 2.0.0-rc6 und 1.8.19

For zeroexport, needs a mqtt connection to a Chint-DTSU, see mqtt.h .

define mostly everything in settings.h:
- runs also as Sniffer (adr 0x00aa, 0x0055, listen everything).
- Channel hopping  TX/RX
- with/without Interrupt,CRC 
- for ZeroExport: connected over MQTT with a DTSU
- output on serial monitor
    serial commands:
    1: help 2:Status 3:PA_LOW 4:PA_HIGH 5:PA_MAX 6:Sniffer 7:ZeroEx 8:OnlyRX 9:ShowTX 10:Wifi 11:CRC 20:WRinfo 21:Gongfa
