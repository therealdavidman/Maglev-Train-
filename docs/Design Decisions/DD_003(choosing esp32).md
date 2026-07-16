
## DD-003

### Decsion
selecting the ESP32-DEVKITC-32UE

#### alternatives

- Arduino uno
- Rasberry pi Pico
- STM32 development boards

#### Requirments:

the controller must:
- control 4 independent electromagnets
- read multiple optical height sensors
- generate high-frequency PWM for the MOSFETS
- execute a PID controll loop with low latency
- support future expansion (current sensing, temperature monitoring, communication)
- be inexpensive and easy to prototype

### Reason

The esp32 was selected because:
- multiple hardware PWM channels suitable for controlling four electromagnets
- sufficient GPIO pins for sensors, MOSFET gate drivers, and future periphrials.
- A 240 MHz dual-core processor capable of executing the levitation control loop with significant performance margin.
- Strong software support through the Arduino framework and ESP-IDF.
- Large community support and extensive documentation, making debugging and development easier.
- Low cost while providing considerably more processing capability than required for the initial prototype.

### Tradeoffs

#### Pros:
- Inexpensive
- Large community and documentation
- High processing performance
- Plenty of GPIO
- Hardware PWM
- Built-in Wi-Fi and Bluetooth for future telemetry or debugging
- Easy to replace and readily available

#### Cons:
- Operates at 3.3 V, requiring level shifting or a gate driver for some power electronics.
- More complex than an Arduino Uno for beginners.
- Wi-Fi/Bluetooth increase power consumption (although they can be disabled).
