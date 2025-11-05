# 🦾 Wireless Operated Robotic Arm Vehicle for Industrial Automation

**Languages & Tools:** Arduino (C/C++) programming , IBT-2 Motor Driver, 8051 Microcontroller Concept, RF Communication, Adrunio IDE, FlySky Transmitter and RF Receiver

---

## 🧠 Project Overview

This project demonstrates a **Wireless Operated Robotic Arm Vehicle** built for **industrial automation** and **remote pick-and-place operations**. It integrates a **robotic arm** on a mobile base, controlled wirelessly using an **RF transmitter-receiver system (Flysky FS-i6X 2.4GHz 6CH RC Transmitter With FS-iA6B 2.4GHz 6CH Receiver)**.

The system uses **Arduino UNO**, **IBT-2 motor drivers**, **ESC (Electronic Speed Controller)**, **Servo Motors** and **11.1V 4500mAh Li-ion Drone Battery Pack** to achieve accurate, smooth motion. It increases **object-handling efficiency by 35%** over manual operation in small industries.

The robot performs the following:

* Wireless **vehicle movement** (Forward, Reverse, Left, Right)
* **Arm lift, grip, and release** via  servo-based gripper for precision handling
* Reliable object transfer on uneven surfaces

---


## 🤖 Prototype Model

![Robotic Arm Vehicle](./1734276429755.jpg)

---

> *Final working model demonstrating object pickup and obstacle handling during Roboveda’23.*
## ⚙️ Hardware Components

| Component                             | Description                                             |
| ------------------------------------- | ------------------------------------------------------- |
| **Microcontroller**                   | Arduino UNO (ATmega328P)                                |
| **Motor Drivers**                     | 2 × IBT-2 Dual H-Bridge Motor Driver Modules            |
| **Power Supply**                      | 11.1V 4200MAH Lipo Battery Pack                         |
| **Motors**                            | 4 DC geared motors (locomotion) + 300RPM Dc Motor       |
| **Gripper**                           | Foam-padded dual-jaw design for soft object handling    |
| **ESC (Electronic Speed Controller)** | 30A Drone Brushless ESC (used for 5V supply regulation) |
| **Servo Motor**                       | 2 x TowerPro MG995 Metal Gear Servo Motor(180º Rotation)|
| **Receiver Module**                   | FS-iA6B 2.4GHz  6 Channels RF Receiver                  |
| **FlySky Transmitter**                | FlySky FS-i6 2.4GHz 6CH  RC Transmitter                 |
---

## 🔌 Circuit Diagram

![Circuit Diagram](./Circuit%20Daigram.jpg)

> The system uses two IBT-2 modules for left and right motor control. Each module receives PWM signals from Arduino pins based on RF receiver input (CH1 & CH2), translating joystick movements into direction and speed.

---

## 💻 Arduino Code

Full Arduino code: [`Robotic Arm Vehicle - Project Code.docx`](./Robotic%20Arm%20Vehicle%20-%20Project%20Code.docx)

**Core Functions:**

* Reads PWM from receiver channels
* Maps input range (960–1980 µs) to speed control
* Drives IBT-2 motor modules for synchronized motion
* Implements safety cutoffs for signal loss

**Code Snippet Example:**

```cpp
// Receiver signal pins
double ch1_pin = 3;
double ch2_pin = 5;

// Right motor driver
int R_EN_right = 2; 
int L_EN_right = 4;
int R_PWM_right = 6;
int L_PWM_right = 9;

// Left motor driver
int R_EN_left = 7; 
int L_EN_left = 8;
int R_PWM_left = 10;
int L_PWM_left = 11;
```

---

## 🧩 Working Principle

1. The transmitter sends analog PWM signals via RF (2.4GHz).
2. The receiver decodes these and passes them to Arduino input pins.
3. Arduino reads pulse width to interpret joystick direction (forward/reverse/turn).
4. PWM outputs control the IBT-2 modules for wheel and arm actuation.
5. The robotic arm performs precise pick, lift, and place operations based on control input.

---

## 🏆 Achievements

### **Cozmo Clench – Roboveda’23 (Sreenidhi Institute of Science & Technology, Hyderabad)**

* **Award:** 🥇 *Certificate of Excellence – First Place*
* **Prize:** ₹9000 cash award
* **Event:** *Samanvayi-Cozmo Clench – Pick and Place Robotics Challenge*
* **Recognition:** For innovation, precise control, and technical excellence
* **Judging Parameters:** Motion stability, mechanical design, Tasks sloving and automation efficiency

📸 **Competition Highlights:**
![Competition Shots 1](Arm_RoboBot.jpg)
![Competition Shots 2](./1734276429755.jpg)

🎥 **Demo Video:** [Watch the Project in Action](./Cosmoclench%20vedio%201%20.mp4)

---

## 📐 System Design & Functionality

| Operation                 | Function                                                    |
| ------------------------- | ----------------------------------------------------------- |
| **Forward / Reverse**     | PWM mapped from CH1 & CH2 joystick inputs                   |
| **Left / Right Turn**     | Differential speed control between left/right IBT-2 modules |
| **Lift / Grip / Release** | Controlled by DC actuator for arm movement                  |
| **Failsafe Idle**         | Automatic stop when receiver signal is lost                 |

---

## 🚀 Key Features

* 2.4GHz RF wireless control system.
* Dual motor synchronization using PWM modulation.
* Efficient, low-latency control for precise motion.
* Simple, scalable design suitable for research and industrial applications.
* Compatible with Arduino IDE and generic motor driver hardware.

---

## 🔮 Future Enhancements

* Replace RF with **Wi-Fi / Bluetooth** for long-range control
* Add **ultrasonic obstacle detection**

---

## 💬 Contact

📧 **Email:** [pavankumar.b.reddy@email.com](mailto:pavankumar.b.reddy@email.com)
🔗 **LinkedIn:** [Pavan Kumar Reddy](https://www.linkedin.com/in/pavankumarreddy7/)

---

> *“Automation doesn’t replace effort — it amplifies precision, creativity, and impact.”*
> — **Pavan Kumar Reddy**

