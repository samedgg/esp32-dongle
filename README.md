## Project Overview

This project introduces a highly integrated, four-layer printed circuit board meticulously designed as an ultra-compact ESP32-C3 Wi-Fi and Bluetooth LE dongle platform. At the core of the system is the Espressif ESP32-C3 SoC (RISC-V 32-bit single-core architecture) handling main control logic, peripheral management, and 2.4 GHz wireless communications. The board integrates an onboard Meandered Inverted-F Antenna (MIFA) engineered for high radiation efficiency and optimal return loss in a compact footprint. The architecture leverages a strict four-layer stackup comprising high-speed and RF signals on the outer layers, an unbroken internal ground plane, and an isolated 3.3V star-routed power plane to guarantee maximum signal integrity and low-noise power delivery. Furthermore, the board features a modern array of interfaces, including a USB Type-C receptacle with dedicated ESD protection, an external SPI NOR Flash, an onboard 6-axis Inertial Measurement Unit (IMU), and an auxiliary UART header for debugging and flashing. All guidelines which are utilized added as folder.

## 3D Views and Schematics

The physical layout and component placement were optimized for mechanical compactness and electrical isolation, ensuring that high-frequency RF domains do not couple noise into the power regulation circuitry or sensitive analog sensor domains. The schematic design is cleanly partitioned into modular functional blocks, distinctly separating the core MCU, power regulation, IMU sensor, and RF matching network.

**3D Board Renders:**

<img width="719" height="809" alt="3d" src="https://github.com/user-attachments/assets/7bf23844-93c2-48e4-a239-6bc29f8bd77d" />

**Schematics:**

<img width="3509" height="2481" alt="schematic" src="https://github.com/user-attachments/assets/4b05d4c1-4089-4208-a6da-e28412e0bd67" />

## Layers

The layer stackup was engineered to provide optimal return paths, minimal loop inductance, and robust thermal dissipation. Layer 1 accommodates the 50-ohm RF trace and mixed-signal routing, Layer 2 functions as an unbroken ground reference plane, Layer 3 delivers 3.3V power via star-routed branches shielded by ground copper, and Layer 4 provides a solid bottom ground plane completing a localized Faraday cage structure.

<img width="716" height="821" alt="layers" src="https://github.com/user-attachments/assets/b5453bd6-5289-468d-98d4-4ca2cba8fd84" />
<img width="687" height="812" alt="l1" src="https://github.com/user-attachments/assets/ea4a2612-e60d-4ed3-9de6-c7c1170333f7" />
<img width="669" height="803" alt="L2" src="https://github.com/user-attachments/assets/8b368977-789e-40cf-b588-6e3678bd2a37" />
<img width="657" height="759" alt="l3" src="https://github.com/user-attachments/assets/99d42547-b4d6-427a-9afd-ad65d5a38eed" />
<img width="655" height="781" alt="l4" src="https://github.com/user-attachments/assets/7bf33f4d-579a-4560-8bf1-b9010ec97a5b" />



## Bill of Materials

| Designator | Component | Description |
| :--- | :--- | :--- |
| **U1** | ESP32-C3 | 32-bit RISC-V Single-Core 2.4 GHz Wi-Fi & BLE 5.0 SoC |
| **U2** | W25Q16JVUXIQ | 16M-bit Serial NOR Flash Memory |
| **U3** | SPX3819M5-L-3-3/TR | 500 mA Low-Noise LDO Voltage Regulator (3.3V) |
| **U4** | BMI088 | 6-Axis High-Performance Inertial Measurement Unit (IMU) |
| **D1, D5** | USBLC6-2SC6 | Low-Capacitance ESD Protection Diode Array |
| **Y1** | 40 MHz Crystal | 40 MHz (±10 ppm) Fundamental SMD Crystal Oscillator |
| **J1** | TYPE-C-31-M-12 | USB Type-C 16-Pin Receptacle |
| **P1** | TSW-104-08-L-S | 4-Pin Auxiliary UART Interface Header |
| **ANT1** | 2.4 GHz MIFA | Onboard Meandered Inverted-F PCB Antenna |
| **L2, C13, C14** | Pi-Matching Network | 0402 / 0201 RF Impedance Matching & Harmonic Filter |

