# esp8266-temp
ESP8266-based temperature sensor

# Getting started

This is what you need to get this code running an your ESP 8266 with an
DS18B20 temperature sensor.

## Prerequisites

1. Get a firmware from https://nodemcu-build.com/. Make sure to have
`encoder` and `1-Wire` in addition to the already selected modules
enabled.
2. Flash your firmware:

	esptool.py --port /dev/ttyUSB0 write_flash --flash_mode dio 0x00000 nodemcu-master-10-modules-2017-08-08-19-33-52-integer.bin


## Setup wifi and copy to esp8266

1. Copy `setup.lua.tpl` to `setup.lua` and set your wifi data.
2. Run the following to upload the lua files:

	nodemcu-uploader.py --port /dev/ttyUSB0 --baud 115200 upload *.lua
