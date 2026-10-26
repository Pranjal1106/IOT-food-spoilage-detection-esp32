# IoT Food Storage Monitoring & Spoilage Detection (ESP32)

An IoT system that monitors temperature, humidity and gas levels inside food storage and raises an alert when conditions become unsafe, helping reduce food spoilage.

## Project status
| Stage | Status |
|---|---|
| Circuit design and simulation in Proteus (Arduino Uno) | Done |
| ESP32 hardware build | In progress |

## How it works
1. The **DHT22** measures temperature and humidity.
2. The **MQ135** gas sensor measures gas levels in the storage area.
3. The microcontroller reads both sensors and shows live values and a status message on an **I2C OLED display**.
4. When a reading crosses the safe limit, the system turns on a **relay**, a **buzzer** and an **LED** as alerts.

## Components
- Arduino Uno (used in the Proteus simulation)
- ESP32 (target board for the hardware build)
- DHT22 temperature and humidity sensor
- MQ135 gas sensor
- 128x64 OLED display (I2C)
- Relay driven by a 2N2222 transistor, with a 1N4007 flyback diode
- Buzzer and LED
- Resistors (10k pull-up on the DHT22 data line, 220 ohm for LED and transistor base)

## Interfaces used
- **I2C**: OLED display
- **UART**: serial output (virtual terminal in the simulation)

## Simulation
![Proteus schematic](images/proteus.png)

## Repository structure
```
code/         Arduino sketch (.ino)
simulation/   Proteus project file (.pdsprj)
images/       Schematic and photos
```

## Next steps
- Build and test the ESP32 hardware version
- Add photos and a short demo video of the working circuit

## Author
**Pranjal Kumawat**, B.Tech Electronics and Communication Engineering, SKIT Jaipur
[LinkedIn](https://linkedin.com/in/pranjalkumawatt)
