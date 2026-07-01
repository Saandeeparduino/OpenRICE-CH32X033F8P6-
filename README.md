# OpenRISC Development Board — CH32X033F8P6
 
> An open-source RISC-V based embedded development platform designed and developed by **Vishishta Innovators**.
 
 <img width="250" height="350" alt="image" src="https://github.com/user-attachments/assets/5828ecea-6f87-4235-821f-15c5ce70c123" />
<img width="525" height="375" alt="image" src="https://github.com/user-attachments/assets/894d95db-362d-4fcf-b62b-df4829a2b5ff" />

---
 
## 📖 Introduction
 
The **OpenRISC Development Board** is an open-source RISC-V based embedded development platform. Its primary goal is to provide students, educators, makers, and embedded system developers with an affordable and easy-to-use hardware platform for learning modern microcontroller programming, RISC-V architecture, and embedded system design.
 
This project focuses on **open hardware**, **practical learning**, and **community-driven development**, enabling users to understand both hardware and software from the ground up.
 
---
 
## 🎯 Background
 
Many commercially available development boards require external programmers, complex hardware setups, or proprietary tools — making them less accessible for beginners and educational institutions.
 
To address these challenges, the team at Vishishta Innovators started the OpenRISC project with the vision of creating a **compact, low-cost, and fully open** development platform.
 
### Key Features (in progress)
 
- 🔓 Open-source hardware and documentation
- 🔌 Arduino IDE compatibility
- 🖥️ USB programming and debugging support
- 🛠️ Integrated programmer/debugger for simplified development
- 📐 Easy PCB design suitable for learning and manufacturing
- 🎓 Educational focus for schools, colleges, and makerspaces
- 📈 Expandable architecture for future OpenRISC board versions
The long-term objective is to build a complete ecosystem that helps students move from basic embedded programming to professional product development.
 
---
 
## ✅ Current Achievements
 
- Custom development board designed by Vishishta Innovators
- Educational hardware suitable for embedded learning
- Open-source PCB and hardware design
- Foundation for future OpenRISC ecosystem development
- Designed with affordability and ease of use in mind
- Community-driven project encouraging contributions and innovation
## 🛣️ Future Roadmap
 
- [ ] Integrated  programmer/ Serial debugger
- [ ] Arduino Board Manager support
- [ ] Example projects and tutorials
- [ ] Complete documentation
- [ ] Expansion boards and accessories
- [ ] Open-source firmware and software tools
---
 
## 🚀 Getting Started — How to Use OpenRISC V1
 
### 1. Install Arduino IDE
 
Download and install the latest [Arduino IDE](https://www.arduino.cc/en/software) for your operating system.
 
### 2. Install the CH32 Arduino Core
 
Install the **CH32 Arduino Core** maintained by [@maxint-rd](https://github.com/maxint-rd) (OpenRISC V1 currently uses this fork, which includes support for the CH32X033 series).
 
> After installation, restart the Arduino IDE.
 
### 3. Install the CH372 USB Driver (Windows Only)
 
For Windows users, install the **CH372 USB driver** so that the board is correctly recognized by the WCH flashing utility.
 
> **Note:** This step is only required on Windows.
 
### 4. Create Your Arduino Sketch
 
Write your Arduino program as you normally would. Example:
 
```cpp
void setup() {
  pinMode(PA6, OUTPUT);  // PA6 IS CONNECTED ONBOARD LED
}
 
void loop() {
  digitalWrite(PA6, HIGH);
  delay(500);
  digitalWrite(PA6, LOW);
  delay(500);
}
```
 
### 5. Select the Correct Board
 
From the Arduino IDE menu:
 
```
Tools → Board → CH32X035 Series
```
 
Then select:
 
```
Tools → Variant → CH32X033F8P6
```
 
### 6. Compile the Sketch
 
Choose:
 
```
Sketch → Export Compiled Binary
```
 
Arduino IDE will generate the compiled firmware files (`.bin` and `.hex`) inside your Arduino sketch folder.
 
### 7. Open WCH Tool
 
Launch the **WCH flashing utility** and configure the following:
 
| Setting | Value |
|---|---|
| Processor | RISC-V |
| Chip Series | CH32X033 |
| Chip Variant | CH32X033F8Px |
| Connection Mode | USB |
| Download Mode | Auto Download |
 
### 8. Select the Firmware
 
Browse to your Arduino sketch folder and select either `project_name.bin` or `project_name.hex`.
 
### 9. Enter Bootloader Mode
 
1. Disconnect the OpenRISC board from the computer.
2. Press and hold the **BOOT** button.
3. Connect the USB cable.
4. Release the **BOOT** button after the board is detected.
The board will enter the built-in USB bootloader.
 
### 10. Flash the Firmware
 
Click **Download** (or **Start**) in the WCH Tool. The firmware is typically programmed in about **2 seconds**.
 
Once programming is complete, reset the board and your Arduino sketch will begin running. 🎉
 
---
 
## 🔄 Flashing Workflow
 
```
Arduino IDE
     │
     ▼
Export Compiled Binary
     │
     ▼
.bin / .hex File
     │
     ▼
WCH Tool
     │
     ▼
USB Bootloader
     │
     ▼
OpenRISC V1 Board
```
 
---
 
## 🤝 Contributing
 
This is a community-driven project — contributions, issues, and feature requests are welcome! Feel free to check the [issues page](../../issues) or open a pull request.
 
---
 
## 📜 License
 
This project is open-source. See the `LICENSE` file for details.
 
---
 
## 👥 Developed By
 
**Vishishta Innovators**
 
> *Vision: Making Embedded Systems and RISC Technology Accessible for Everyone.*
