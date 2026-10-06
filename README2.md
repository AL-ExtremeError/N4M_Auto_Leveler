# N4M_Auto_Leveler

A hardware and software solution for enabling automatic bed leveling and Z-offset calibration on the Elegoo Neptune 4 Max 3D printer. This project integrates the **RP2040 Zero**, **HX711 ADC**, and **logic level converter** to eliminate manual calibration, improve print quality, and ensure consistent first-layer adhesion.

---

## 📌 Project Overview

The Elegoo Neptune 4 Max Auto-Z-Offset & Auto-Leveling Sensor System leverages the **RP2040 Zero** microcontroller, **HX711 ADC**, and a **logic level converter** to enable precise, automated bed leveling and Z-offset calibration. This integration ensures seamless compatibility with the printer’s firmware, enhancing print quality and eliminating the process of manual calibration (Z-Offset) efforts.

---

## 📚 Description

### How It Works

The system uses strain gauge sensors connected to the HX711 ADC to measure bed surface irregularities. The RP2040 Zero processes this data in real time, calculates the required Z-offset adjustments, and communicates with the printer’s firmware (via serial or G-code) to apply corrections.

### Compatibility Notes

- Works with Elegoo Neptune 4 Max firmware versions **1.2.0+**.
- Ensure your printer’s firmware is updated before installation.

### Hardware Requirements

- RP2040 Zero (with USB-C port)
- HX711 ADC module
- Logic level converter (3.3V ↔ 5V)
- Strain gauge sensors (for bed leveling)

---

## 🔧 Key Features

- **Precision**: High-resolution HX711 ADC for accurate sensor readings.
- **Compatibility**: Works seamlessly with Elegoo Neptune 4 Max firmware.
- **Automation**: Reduces manual intervention for bed leveling and Z-offset calibration.
- **Reliability**: Logic level converter ensures stable communication between 3.3V and 5V components.

---

## 🛠️ Printer.cfg Configuration

Modify the `printer.cfg` file in your Elegoo Neptune 4 Max firmware to include the following settings:

```ini
[auto_leveler]
sensor_type: hx711
serial_port: /dev/ttyACM0
```

Ensure the `serial_port` matches the RP2040 Zero’s connection.

---

## 📥 Installation Guide

1. **Assemble Hardware**: Connect the HX711 ADC to the strain gauge sensors and logic level converter.
2. **Flash Firmware**: Use the provided firmware file to program the RP2040 Zero.
3. **Configure Printer**: Update `printer.cfg` with the auto-leveler settings.
4. **Test System**: Run a test print to verify sensor calibration and auto-leveling functionality.

---

## 📝 Usage

- **Activate Auto-Leveling**: Enable the auto-leveler feature in your printer’s firmware settings.
- **Monitor Sensor Data**: Use the RP2040’s debug output to verify sensor readings and Z-offset adjustments.
- **Calibrate Sensors**: Follow the on-screen prompts to recalibrate sensors if needed.

---

## 🛠️ Troubleshooting

- **No Sensor Data Detected**: Check HX711 wiring and ensure the logic level converter is properly connected.
- **Z-Offset Not Applying**: Verify the `serial_port` in `printer.cfg` matches the RP2040 Zero’s connection.
- **Printer Not Recognizing Auto-Leveler**: Ensure firmware is updated to **1.2.0+** and the `auto_leveler` section is correctly configured.

---

## 🤝 Contributing

- **Bug Reports**: Submit issues via [GitHub Issues](https://github.com/AL-ExtremeError/N4M_Auto_Leveler/issues).
- **Feature Requests**: Propose enhancements via [GitHub Discussions](https://github.com/AL-ExtremeError/N4M_Auto_Leveler/discussions).
- **Code Contributions**: Fork the repository, make changes, and submit a pull request.

---

## 📌 Updates Log

[View Updates Log](https://github.com/AL-ExtremeError/N4M_Auto_Leveler/wiki/Updates-Log)

---

This solution is ideal for users seeking a cost-effective, customizable upgrade to their 3D printer’s auto-leveling capabilities.