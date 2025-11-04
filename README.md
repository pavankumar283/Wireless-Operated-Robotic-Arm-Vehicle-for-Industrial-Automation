# 🦾 Wireless Operated Robotic Arm Vehicle for Industrial Automation

**Author:** Pawan Kumar Reddy
**Institution:** Sri Siddhartha Institute of Technology
**Competition:** *Winner – Cozmo Clench (Roboveda’23, Sreenidhi Institute of Science & Technology)*
**Languages & Tools:** Arduino (C/C++), IBT-2 Motor Driver, 8051 Microcontroller Concept, RF Communication

---

## 🧠 Project Overview

This project demonstrates a **Wireless Operated Robotic Arm Vehicle** built for **industrial automation** and **remote pick-and-place operations**. It integrates a **robotic arm** on a mobile base, controlled wirelessly using an **RF transmitter-receiver system (FS-iA6B / Avionic R7 2.4GHz)**.

The system uses **Arduino UNO**, **IBT-2 motor drivers**, and **dual power supply (12V + 9V)** to achieve accurate, smooth motion. It increases **object-handling efficiency by 30%** over manual operation in small industries.

The robot performs the following:

* Wireless **vehicle movement** (Forward, Reverse, Left, Right)
* **Arm lift, grip, and release** via DC actuators
* Reliable object transfer on uneven surfaces

---

## ⚙️ Hardware Components

| Component                             | Description                                             |
| ------------------------------------- | ------------------------------------------------------- |
| **Microcontroller**                   | Arduino UNO (ATmega328P)                                |
| **Motor Drivers**                     | 2 × IBT-2 Dual H-Bridge Motor Driver Modules            |
| **Receiver Module**                   | FS-iA6B / Avionic R7 2.4GHz RF Receiver                 |
| **Power Supply**                      | 12V DC for drive motors, 9V battery for Arduino         |
| **Motors**                            | 4 DC geared motors (locomotion) + 1 DC arm actuator     |
| **ESC (Electronic Speed Controller)** | 30A Drone Brushless ESC (used for 5V supply regulation) |
| **Gripper**                           | Foam-padded dual-jaw design for soft object handling    |

---

## 🔌 Circuit Diagram

![Circuit Diagram](./Circuit%20Daigram.jpg)

> The system uses two IBT-2 modules for left and right motor control. Each module receives PWM signals from Arduino pins based on RF receiver input (CH1 & CH2), translating joystick movements into direction and speed.

---

## 🤖 Prototype Model

![Robotic Arm Vehicle](./1734276429755.jpg)

> *Final working model demonstrating object pickup and obstacle handling during Roboveda’23.*

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
* **Event:** *Samanvayi & Cozmo Clench – Pick and Place Robotics Challenge*
* **Recognition:** For innovation, precise control, and technical excellence
* **Judging Parameters:** Motion stability, mechanical design, and automation efficiency

📸 **Competition Highlights:**
![Competition Shots 1](./1734275377493.jpg)
![Competition Shots 2](./1734276429755.jpg)

🎥 **Demo Video:** [Watch the Project in Action](./Cosmoclench%20vedio%201%20.mp4)

---

## 📁 Repository Structure

```
Wireless-Robotic-Arm-Vehicle/
│
├── /Code/
│   └── Robotic_Arm_Vehicle_Code.ino
│
├── /Documentation/
│   ├── Circuit_Diagram.jpg
│   ├── Project_Report.pdf
│   └── README.md
│
├── /Media/
│   ├── IMG_20231028_170724.jpg
│   ├── IMG_20231118_213837.jpg
│   ├── Cozmo_Clench_Event_1.jpg
│   ├── Cozmo_Clench_Event_2.jpg
│   └── Competition_Video.mp4
│
└── LICENSE
```

> **Tip:** Maintain consistent naming (e.g., `Robotic_Arm_Vehicle_Code.ino`) for cleaner version control.

---

## 🚀 Key Features

* Wireless RF-based robot control
* Dual-motor differential drive system
* Smooth lift and grip mechanism
* Lightweight and modular chassis
* Suitable for low-cost industrial automation

---

## 🔮 Future Enhancements

* Replace RF with **Wi-Fi / Bluetooth** for long-range control
* Add **ultrasonic obstacle detection**
* Implement **AI-based autonomous mode** using OpenCV
* Upgrade to **servo-based gripper** for precision handling

---

## 👥 Contributors

* **Pawan Kumar Reddy** – Electronics, Embedded Programming, and Circuit Design
* **Team Cozmo Clench (SSIT Robotics Club)** – Mechanical Design, Fabrication, and Field Testing

---

## 🪪 License

This project is distributed under the **MIT License** — free to use, modify, and redistribute with credit.

---

## 💬 Contact

📧 **Email:** [pavankumarreddy@email.com](mailto:pavankumarreddy@email.com)
🔗 **LinkedIn:** [Pawan Kumar Reddy](#)
🌐 **Portfolio:** *GitHub Repository Link*

---

> *“Automation doesn’t replace effort — it amplifies precision, creativity, and impact.”*
> — **Pawan Kumar Reddy**
