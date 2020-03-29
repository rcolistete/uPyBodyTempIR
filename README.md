# uPyBodyTempIR

### uPyBodyTempIR -  Body Temperature IR Meter with MLX90615 sensor and MicroPython microcontroller

### Goal : a low cost and open device to detect human body (head) temperature to help detect fever (due to covid-19 or not), using IoT.

The [I2C sensor MLX90615](https://www.melexis.com/en/product/mlx90615/) is a infrared thermometer for non-contact temperature measurements, with accuracy of +/- 0.2 C for human temperatures, so fever can be detected.

Another sensor can be useful to avoid people interfacing with physical contact, it is the I2C sensor I2C [APDS-9960 Digital RGB, Ambient Light, Proximity and Gesture Sensor](https://www.broadcom.com/products/optical-sensors/integrated-ambient-light-and-proximity-sensors/apds-9960). See this excellent [guide from Adafruit](https://www.adafruit.com/product/3595). APDS-9960 supports 4 simple gestures (left to right, right to left, up to down, down to up) directly but other combined gestures are possible by programming.

The components of one possible configuration is uPyBodyTempIR-M5StickC : 
- MLX90615;
- (optional) APDS-9960;
- [M5StickC](https://docs.m5stack.com/#/en/core/m5stickc), which is a ESP32 (WiFi + Bluetooth) + screen + 2 buttons + battery + connectors + case + etc.
- accessories (board, wires, etc).

The development will use MicroPython. Initial versions will have only local screen output. The IoT will be added by using WiFi + MQTT + IoT Cloud (to be chosen) to send the temperature measurements, visualize plot, have alarm of high body temperature, etc.
