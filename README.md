# OpenRICE-CH32X033F8P6-
The OpenRISC Development Board is an open-source RISC-based embedded development platform designed and developed by Vishishta Innovators.

Introduction

The OpenRISC Development Board is an open-source RISC-based embedded development platform designed and developed by Vishishta Innovators. The primary goal of this project is to provide students, educators, makers, and embedded system developers with an affordable and easy-to-use hardware platform for learning modern microcontroller programming, RISC architecture, and embedded system design.

This project focuses on open hardware, practical learning, and community-driven development, enabling users to understand both hardware and software from the ground up.

Background

Many commercially available development boards require external programmers, complex hardware setups, or proprietary tools, making them less accessible for beginners and educational institutions.

To address these challenges, our team at Vishishta Innovators started the OpenRISC project with the vision of creating a compact, low-cost, and fully open development platform.

The project is being designed with features such as:

Open-source hardware and documentation
Arduino IDE compatibility
USB programming and debugging support
Integrated programmer/debugger for simplified development
Easy PCB design suitable for learning and manufacturing
Educational focus for schools, colleges, and makerspaces
Expandable architecture for future OpenRISC board versions

The long-term objective is to build a complete ecosystem that helps students move from basic embedded programming to professional product development.

Outcome

The OpenRISC Development Board represents an important step toward accessible embedded system education.

Current achievements include:

✅ Custom development board designed by Vishishta Innovators
✅ Educational hardware suitable for embedded learning
✅ Open-source PCB and hardware design
✅ Foundation for future OpenRISC ecosystem development
✅ Designed with affordability and ease of use in mind
✅ Community-driven project encouraging contributions and innovation

Future roadmap:

Integrated USB programmer/debugger
Arduino Board Manager support
Example projects and tutorials
Complete documentation
Expansion boards and accessories
Open-source firmware and software tools

Developed by: Vishishta Innovators
Vision: Making Embedded Systems and RISC Technology Accessible for Everyone.


//--------------------------------------------------------------------------------------------------------//
How to Use OpenRISC V1
1. Install Arduino IDE

Download and install the latest Arduino IDE for your operating system.

2. Install the CH32 Arduino Core

Install the CH32 Arduino Core maintained by @maxint-rd (OpenRISC V1 currently uses this fork, which includes support for the CH32X033 series).

After installation, restart the Arduino IDE.

3. Install the CH372 USB Driver (Windows Only)

For Windows users, install the CH372 USB driver so that the board is correctly recognized by the WCH flashing utility.

Note: This step is only required on Windows.

4. Create Your Arduino Sketch

Write your Arduino program as you normally would.

Example:

void setup() {
  pinMode(PC0, OUTPUT);
}

void loop() {
  digitalWrite(PC0, HIGH);
  delay(500);
  digitalWrite(PC0, LOW);
  delay(500);
}
5. Select the Correct Board

From the Arduino IDE menu:

Tools → Board → CH32X035 Series

Then select:

Tools → Variant → CH32X033F8P6
6. Compile the Sketch

Choose:

Sketch → Export Compiled Binary

Arduino IDE will generate the compiled firmware files:

.bin
.hex

These files are saved inside your Arduino sketch folder.

7. Open WCH Tool

Launch the WCH flashing utility.

Configure the following:

Processor: RISC-V
Chip Series: CH32X033
Chip Variant: CH32X033F8Px
Connection Mode: USB
Download Mode: Auto Download
8. Select the Firmware

Browse to your Arduino sketch folder and select either:

project_name.bin
or
project_name.hex
9. Enter Bootloader Mode
Disconnect the OpenRISC board from the computer.
Press and hold the BOOT button.
Connect the USB cable.
Release the BOOT button after the board is detected.

The board will enter the built-in USB bootloader.

10. Flash the Firmware

Click Download (or Start) in the WCH Tool.

The firmware is typically programmed in about 2 seconds.

Once programming is complete, reset the board and your Arduino sketch will begin running.

Flashing Workflow
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
