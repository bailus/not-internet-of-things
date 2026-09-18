# Not Internet of Things

Replacing the firmware on IoT devices to defend against [enshittification](https://craphound.com/category/enshittification/).

Some devices can be flashed over the network, but most require connecting wires to the serial port on the device.

## Flashing guides
My guides for flashing some of the popular cheap devices available in New Zealand (and Australia):

### Light bulbs
* [Brilliant 21893](Brilliant%2021893/readme.md): Brilliant Lighting Model 21893, E14 (Australia / New Zealand). CCT+RGB, 4.3W 220V-240V.
* [Kogan KAE27RGBC1A](Kogan%20KAE27RGBC1A/readme.md): Kogan RGB+CCT Smart WiFi Light Bulb. Model KAE27RGBC1A. E27, 240V, 10W.

### Plugs
* [Brilliant 21883/05](Brilliant%2021883%2005/readme.md): Brilliant Smart WiFi Double Wall Plug with USB-C & USB-A Port, 240V.

## Open source firmwares
### Tasmota
[Documentation](https://tasmota.github.io/docs/), [GitHub](https://github.com/arendst/tasmota), [Device database](https://templates.blakadder.com/)

The best option for older devices.
* ESP devices (ESP8266, ESP32)
* Web interface for configuration and control
* Supports MQTT for integration with Home Assistant

### ESPHome
[Documentation](https://esphome.io/), [GitHub](https://github.com/esphome/esphome), [Device database](https://esphome.io/devices/)

If you want more control over on-device logic.
* ESP devices (ESP8266, ESP32)
* YAML-based configuration
* Supports MQTT for integration with Home Assistant

### WLED
[Documentation](https://kno.wled.ge/), [GitHub](https://github.com/Aircoookie/WLED)

For addressable LED strips and complex lighting setups.
* ESP devices (ESP8266, ESP32)
* Web interface for configuration and control
* LED effects and animations
* Supports MQTT for integration with Home Assistant
* Supports DMX over IP for complex multi-device animations and integration with professional lighting control systems

### OpenBK
[Forum](https://www.elektroda.com/rtvforum/forum507.html), [GitHub](https://github.com/openshwprojects/OpenBK7231T_App), [Device database](https://openbekeniot.github.io/webapp/devicesList.html)

Similar to Tasmota, but for devices with Beken chips. A lot of newer Tuya devices use these chips.
* [Beken](https://www.bekencorp.com/en/goods/product/cid/58.html) devices (BK7231N, BK7231T).
* Web interface for configuration and control
* Supports MQTT for integration with Home Assistant

### ATC_MiThermometer
[GitHub](https://github.com/pvvx/ATC_MiThermometer), [Device list](https://pvvx.github.io/), [Web-based flasher](https://pvvx.github.io/ATC_MiThermometer/TelinkMiFlasher.html)

Use cheap bluetooth thermometers without an app.
* Bluetooth thermometers with [Telink chips](https://www.telink-semi.com/products/bluetooth-le/tl721x)
* Supports Bluetooth Low Energy (BLE) and the [BTHome](https://bthome.io/) protocol
* Use a USB Bluetooth adapter on the end of a USB extension cable for a reliable connection to Home Assistant
* Web-based flasher for solder-free installation

### ZigbeeTLc
[GitHub](https://github.com/pvvx/ZigbeeTLc), [Device list](https://pvvx.github.io/), [Web-based flasher](https://pvvx.github.io/ATC_MiThermometer/TelinkMiFlasher.html)

Integrate cheap thermometers into your Zigbee network.
* Bluetooth thermometers with [Telink chips](https://www.telink-semi.com/products/bluetooth-le/tl721x)
* Converts bluetooth devices to Zigbee
* Requires a compatible hardware adapter (Zigbee coordinator) to [connect to Home Assistant](https://www.home-assistant.io/integrations/zha/)
* Web-based flasher for solder-free installation
