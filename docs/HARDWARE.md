# Hardware — IoTMotionDetectionAlarm

## Parts and electrical limits
ESP32 DevKit and PIR motion module; low-voltage active buzzer. Power low-voltage modules from a suitable regulated supply, tie grounds together, and verify signal levels before connection. GPIO34 is input-only and ADC1 is used because ADC2 conflicts with Wi-Fi. Never apply more than 3.3 V to an ESP32 GPIO.

| ESP32 pin | Connection | Requirement |
|---|---|---|
| ESP32 3V3 | sensor VCC | Verify module supply rating |
| ESP32 GND | sensor GND | Common low-voltage ground |
| GPIO27 | digital signal | Use INPUT_PULLUP where switch wiring allows; module output must be 3.3 V |
| GPIO14 | buzzer input | Active high; MOSFET/flyback diode for inductive load |

Use a pull-down on GPIO14's driver input so the load remains off during boot. Low-voltage relays must not be connected directly to GPIO, and inductive loads need flyback protection.

## Sensor specification and calibration
The firmware accepts motion from 0 to 1 boolean. Secondary value is reserved (none). This is a demonstration alarm and cannot replace a monitored security system. Use a multimeter and the sensor data sheet for the exact module revision.
