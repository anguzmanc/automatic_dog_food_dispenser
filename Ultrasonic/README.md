# Ultrasonic Sensor System

This peripheral of the device includes:

- **Input:**  
  An HC-SR04 ultrasonic sensor module used to measure the food level inside the container by calculating the distance between the sensor and the food surface.

- **Outputs:**  
  Three LED indicators:
  
  - 🔴 **Red LED:** Indicates low or empty food level.
  - 🟡 **Yellow LED:** Indicates the container is approximately below half capacity.
  - 🟢 **Green LED:** Indicates the container is full or above half capacity.

<p align="center">
  <img width="80%" alt="RTL Ultrasonido" src="https://github.com/user-attachments/assets/f7543f1d-b492-4d43-8ae1-d22ec24a6178" />
  
</p>

---

# Development

To implement this subsystem, research was conducted on the operating principles of ultrasonic sensors, particularly the HC-SR04 module.

The trigger signal was configured with an activation period of approximately **20 ms**, allowing the sensor to emit ultrasonic pulses toward the food surface inside the container.

A counter inside the FPGA was used to measure the response timing while the ultrasonic pulse traveled and reflected back to the sensor. Based on this measured distance, the corresponding LED indicator was activated according to the detected food level.

---

## 🎥 Distance Sensor Operation Video

[![Distance Sensor Test](https://img.youtube.com/vi/pixdbLauMtA/0.jpg)](https://www.youtube.com/watch?v=pixdbLauMtA)

---

# Challenges

One of the main challenges was calibrating the distance thresholds so the LEDs correctly represented the food level inside the 40 cm container.

The final selected ranges were:

- 🟢 **Green LED:** Activated for distances below **10 cm**
- 🟡 **Yellow LED:** Activated for distances between **10 cm and 20 cm**
- 🔴 **Red LED:** Activated for distances between **20 cm and 40 cm**

An unresolved issue was a slight flickering between the yellow and red LEDs when the red LED became active. This behavior was likely caused by trigger and echo timing adjustments, as well as small variations in the FPGA counting process during distance measurements.

---

# Final Remarks

After several calibration adjustments, the ultrasonic subsystem successfully achieved stable food-level detection and proper LED indication behavior, demonstrating the correct operation of this peripheral within the automatic dog food dispenser prototype.
