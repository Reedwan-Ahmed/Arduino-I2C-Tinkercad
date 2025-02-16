# Arduino-I2C-Tinkercad
Arduino I2C Assignment Codes and Tutorial
This repository contains two Arduino I2C projects designed for Tinkercad simulation.

✅ Project 1: Integer Input with LED and LCD
✅ Project 2: Slide Switch Guessing Game
Both projects use I2C communication between two Arduinos (Master: UNO, Slave: Nano/UNO).

📌 Project 1: Integer Input with LED and LCD
📝 Description
Takes two integer inputs:
m (from Serial Monitor 1 on the Master - UNO).
n (from Serial Monitor 2 on the Slave - Nano/UNO).
Checks condition:
If m > n: Blink LED (on Master) n times.
If m ≤ n: Show m on LCD (connected to Slave).
🔧 How It Works
m (Master Input)	n (Slave Input)	Result
5	4	Blink LED for 4 times
3	3	Show 3 on LCD
3	6	Show 3 on LCD

📌 Project 2: Slide Switch Guessing Game
📝 Description
A slide switch is connected to UNO-2 (Master).
User guesses the switch position by entering "left" or "right" in Serial Monitor.
UNO-2 compares the guess with actual switch position:
If correct: Turn ON LED1 (UNO-2), Turn OFF LED2 (UNO-1/Nano).
If incorrect: Turn OFF LED1 (UNO-2), Turn ON LED2 (UNO-1/Nano).
🔧 How It Works (All 5 Cases)
Slide Switch Position	User Input (Serial Monitor-2)	LED1 (UNO-2)	LED2 (UNO-1/Nano)
left	"Left"	OFF	ON
left	"left"	ON	OFF
right	"back"	OFF	ON
right	"RIGHT"	OFF	ON
right	"right"	ON	OFF
🛠️ Hardware Used
Arduino UNO (Master - UNO-2)
Arduino Nano/UNO (Slave - UNO-1)
I2C Communication (SDA → A4, SCL → A5)
LCD 16x2 (I2C, Address: 0x27, Slave side)
Slide Switch (Master side, connected to A0)
LED1 (Pin 10 on Master - UNO-2)
LED2 (Pin 11 on Slave - UNO-1/Nano)
Resistors (220Ω for LEDs)

🚀 How to Use (Tinkercad Simulation)
Set up the circuit in Tinkercad with two Arduinos (UNO & Nano/UNO).
Upload master.ino to Arduino UNO (Master).
Upload slave.ino to Arduino Nano/UNO (Slave).
Open Serial Monitor for both boards.
For Project 1: Enter values for m and n in respective Serial Monitors.
For Project 2: Move the slide switch and enter a guess in Serial Monitor.
