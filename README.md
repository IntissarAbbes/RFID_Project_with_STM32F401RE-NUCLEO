
# RFID Project with STM32F401RE-Nucleo

![GitHub repo size](https://img.shields.io/github/repo-size/Intissarabbes/RFID_Project_with_STM32F401RE-NUCLEO?color=blue)
![GitHub last commit](https://img.shields.io/github/last-commit/Intissarabbes/RFID_Project_with_STM32F401RE-NUCLEO)
![GitHub language count](https://img.shields.io/github/languages/count/Intissarabbes/RFID_Project_with_STM32F401RE-NUCLEO)
![GitHub top language](https://img.shields.io/github/languages/top/Intissarabbes/RFID_Project_with_STM32F401RE-NUCLEO)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## 📘 Overview
This project implements an **RFID-based reader system** using the **STM32F401RE Nucleo board**.  
The microcontroller communicates with an **RFID module (RC522)** to detect and read RFID cards or tags.  
Status messages are sent via **UART serial communication** to indicate the current operation or any hardware errors.



## 💬 Example Output Messages

```
char *msg1 = "Reading from card \r\n";
char *msg2 = "Reading from TAG \r\n";
char *msg3 = "Hardware ERROR occurred, PLEASE check your RFID Module or Card/TAG !!\r\n";

```

## ⚙️ Hardware Components
- **STM32F401RE Nucleo** board  
- **RFID Reader (RC522 or compatible)**  
- **Jumper wires**  
- **Breadboard (optional)**  
- **3.3V Power Supply**

---

## 🔌 Connections
| RFID Module | STM32F401RE Pin |
|--------------|----------------|
| VCC          | 3.3V           |
| GND          | GND            |
| SDA / NSS    | PB9 (SPI1_NSS) |
| SCK          | PA5 (SPI1_SCK) |
| MOSI         | PA7 (SPI1_MOSI) |
| MISO         | PA6 (SPI1_MISO) |
| RST          | PA8             |

> Adjust pins in STM32CubeMX if you choose different SPI or UART configurations.

---

## 🧰 Software Tools
- **STM32CubeIDE** – Main IDE for code development  
- **STM32CubeMX** – Peripheral configuration and code generation  
- **HAL Library** – For hardware abstraction layer functions  
- **Git + GitHub** – Version control and project hosting  

---

## 🚀 How to Use
1. Clone this repository:
   ```bash
   git clone https://github.com/Intissarabbes/RFID_Project_with_STM32F401RE-NUCLEO.git
2.Open the project in STM32CubeIDE.

3.Connect your STM32 Nucleo board via USB.

4.Build and flash the code to your board.

5.Open a serial monitor (115200 baud) to view detected RFID tag IDs.
