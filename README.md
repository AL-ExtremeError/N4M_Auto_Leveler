[Updates Log](https://github.com/AL-ExtremeError/N4M_Auto_Leveler/wiki/Updates-Log)

This is a Work-In-Progress as of 10/4/2026

# N4M_Auto_Leveler
Walk-Thru for adding sensors for Auto-Z-Offset &amp; Auto-Leveling to an Elegoo Neptune 4 Max 

**Summary**  
The Elegoo Neptune 4 Max Auto-Z-Offset & Auto-Leveling Sensor System leverages the **RP2040 Zero** microcontroller, **HX711 ADC**, and a **logic level converter** to enable precise, automated bed leveling and Z-offset calibration. This integration ensures seamless compatibility with the printer’s firmware, enhancing print quality and eliminating the process of manual calibration (Z-Offset) efforts.  

---

**Description**  
This system utilizes the **RP2040 Zero** as the central controller, processing sensor data from the **HX711** (a 24-bit analog-to-digital converter) to measure and adjust the printer’s Z-axis height automatically. The **HX711** is paired with a **logic level converter** to bridge the voltage difference between the 3.3V RP2040 and the 5V HX711, ensuring stable communication.  

The sensor system works by detecting bed surface irregularities (via strain guage sensors) and calculating the required Z-offset adjustments. The RP2040 processes this data in real time, sending commands to the printer’s firmware to level the bed and optimize the first-layer height. This setup eliminates manual calibration, improves print adhesion, and ensures consistent results across multiple prints.  

**Key Features**  
- **Precision**: High-resolution HX711 ADC for accurate sensor readings.  
- **Compatibility**: Works seamlessly with Elegoo Neptune 4 Max firmware.
	- Printer.cfg modifications need to be made in order to configure
- **Automation**: Reduces manual intervention for bed leveling and Z-offset calibration.  
- **Reliability**: Logic level converter ensures stable communication between 3.3V and 5V components.  

This solution is ideal for users seeking a cost-effective, customizable upgrade to their 3D printer’s auto-leveling capabilities.
