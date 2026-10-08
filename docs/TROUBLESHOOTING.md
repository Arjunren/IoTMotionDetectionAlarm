# Troubleshooting — IoTMotionDetectionAlarm

| Symptom | Check |
|---|---|
| No motion | Verify sensor power, grounds, pin table, voltage limits, and module orientation. |
| Invalid sample | Check 0–1 boolean range and sensor calibration. |
| Wi-Fi disconnected | Check SSID, 2.4 GHz coverage, and local network policy. |
| MQTT disconnected | Check broker DNS, port 8883, CA PEM, device credentials, and publish ACL. |
| Unexpected alert | Inspect raw motion and reserved; calibrate the threshold in `logic.h`. |
| Build failure | Confirm PlatformIO is installed and dependency downloads are permitted. |

This is a demonstration alarm and cannot replace a monitored security system.
