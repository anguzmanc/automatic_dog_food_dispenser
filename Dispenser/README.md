# Gate Control System

This peripheral of the device includes:

- **Input:**  
  An internal FPGA counter acting as a timer. After a predefined time interval, the servomotor moves to open the food gate. A second counter with a shorter period keeps the gate open for a few seconds before closing it again.

- **Output:**  
  An SG90 servomotor, which acts as the mechanical gate that allows food to pass through whenever it receives the activation signal from the counter.

<p align="center">
  <img width="80%" alt="RTL Compuerta" src="https://github.com/user-attachments/assets/93de9d93-4e55-4b0f-9e84-185e3e52751d" />
</p>

---

# Development

To implement this subsystem, the code developed during the second laboratory practice was reused, where the same servomotor was previously controlled using an FPGA switch.

This functionality was adapted into a fully automatic process, eliminating the need for external manual activation. Two additional modules were implemented:

1. A frequency divider module, used to generate a lower frequency signal that simplified timing control for the servomotor operation.

2. An automatic control module (`automatico.v`), responsible for handling the opening and closing sequence:
   - A primary counter activates the servomotor after a predefined waiting period.
   - A secondary counter keeps the gate open for a shorter interval before closing it again.

The servomotor successfully achieved a 180° rotation based on its specifications:
- A pulse width of approximately **100 µs** corresponded to the 0° position.
- A pulse width near **2.1 ms** generated the expected 180° rotation.

For the timing system:
- The gate remained closed for approximately **26 seconds**
- The gate stayed open for approximately **3 seconds** before closing again.

---

## 🎥 Gate Operation Video

[![Gate Operation](https://img.youtube.com/vi/dtkBmaRJkPA/0.jpg)](https://www.youtube.com/watch?v=dtkBmaRJkPA)

---

# Challenges

One of the main difficulties was synchronizing the servomotor timing with the required counter bit sizes inside the `automatico.v` module.

Initially, using a high frequency after the frequency division caused the servomotor to operate too quickly, resulting in unstable behavior. After several adjustments, a working frequency close to **300 Hz** was selected, allowing proper counting and smoother gate opening and closing intervals suitable for the prototype demonstration.

---

# Final Remarks

After solving the synchronization and timing issues, the gate control subsystem achieved stable and correct operation, successfully demonstrating the functionality of this peripheral within the automatic dog food dispenser prototype.
