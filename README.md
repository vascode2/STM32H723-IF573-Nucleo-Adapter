# STM32H7 Nucleo Wi-Fi 6E Integration (Adapter Card)

**A stackable Wi-Fi 6E integration on the NUCLEO-H723ZG using the Ezurio STM32 Nucleo Adapter Card.**

![Project Status](https://img.shields.io/badge/Status-Finished-success)
![Hardware](https://img.shields.io/badge/Hardware-NUCLEO--H723ZG-blue)
![Connectivity](https://img.shields.io/badge/Module-Sona_IF573_(WiFi_6E)-orange)

## 📖 Overview
This project demonstrates how to integrate the **Ezurio (Laird Connectivity) Sona IF573** (Wi-Fi 6E) module with the **STM32 NUCLEO-H723ZG** development board.

Unlike integrations requiring manual soldering, this project utilizes the **Ezurio STM32 Nucleo Adapter Card**. This enables a **stackable, plug-and-play connection** via the Nucleo-144 headers, allowing for rapid prototyping without hardware modification.

**Key Technical Challenge:** The NUCLEO-H723ZG has a limit of **1MB Flash memory**. To successfully port the Infineon AIROC™ Wi-Fi stack, this project utilizes a custom build configuration that strips out non-essential utilities (like `iperf`), ensuring the final binary image fits successfully within the <1MB flash constraint.

## 🛠️ Tech Stack
* **MCU:** STM32H723ZG (Cortex-M7 @ 550MHz)
* **Wireless:** Sona IF573 (Infineon CYW55572)
* **Interface:** M.2 to Nucleo-144 Adapter (SDIO)
* **RTOS:** FreeRTOS
* **Optimization:** Binary image reduction for <1MB Flash targets.

## 📂 Documentation
The full application note is hosted in this repository and also published online.

### 🌐 [View the Official Published Guide](https://lairdcp.github.io/guides/IF573-NUCLEO-H723ZG/1.0/IF573_NUCLEO_H723ZG_AppNote.html)

You can also view the local version in the `docs` folder:

### [👉 Read the Local Integration Guide](docs/IF573_NUCLEO_H723ZG_AppNote.md)

* **Hardware Setup:** Utilizing the Nucleo Adapter Card for instant connectivity.
* **Firmware Porting:** Migrating the AIROC stack to the H723ZG.
* **Flash Optimization:** Reducing the generated image size to accommodate the 1MB limit.

## 📦 Resources
* **Source Code:** [wifi_bt_tester_H723ZG.zip](docs/source/wifi_bt_tester_H723ZG.zip) (Customized project files).
* **Hardware Used:** NUCLEO-H723ZG, Ezurio Nucleo Adapter Card, Sona IF573.

---
*Disclaimer: This project requires the specific Ezurio Adapter Card for correct pin mapping.*
