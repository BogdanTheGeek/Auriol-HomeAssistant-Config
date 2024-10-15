# Connecting a Auriol Weather Station to Home Assistant

## Requirements
 - Any SDR(Software Defined Radio) supported by [rtl_433](https://github.com/merbanan/rtl_433)
 - Home Assistant
 - MQTT Broker Setup with Home Assistant
 - [rtl_433](https://github.com/merbanan/rtl_433)

## Configuring rtl_433
```sh
rtl_433 -R 19 -F 'mqtt://0.0.0.0:1883,retain=0,events=sensors/weather-station/[model:UNKNOWN]/id-[id:000]/sensor-[channel:0]' -M time:iso:tz -M level
```
## Configuring Home Assistant
Check [configuration.yaml](configuration.yaml)
