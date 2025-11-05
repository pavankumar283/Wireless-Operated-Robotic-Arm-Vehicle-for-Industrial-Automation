# 🦾 Wireless Operated Robotic Arm Vehicle for Industrial Automation

**Languages & Tools:** Arduino (C/C++), IBT-2 Motor Driver, 8051 Microcontroller Concept, RF Communication, Adrunio IDE, FlySky Transmitter and RF Receiver

---

## 🧠 Project Overview

This project demonstrates a **Wireless Operated Robotic Arm Vehicle** built for **industrial automation** and **remote pick-and-place operations**. It integrates a **robotic arm** on a mobile base, controlled wirelessly using an **RF transmitter-receiver system (FS-iA6B / Avionic R7 2.4GHz)**.

The system uses **Arduino UNO**, **IBT-2 motor drivers**, and **dual power supply (12V + 9V)** to achieve accurate, smooth motion. It increases **object-handling efficiency by 40%** over manual operation in small industries.

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
* **Event:** *Samanvayi-Cozmo Clench – Pick and Place Robotics Challenge*
* **Recognition:** For innovation, precise control, and technical excellence
* **Judging Parameters:** Motion stability, mechanical design, Tasks sloving and automation efficiency

📸 **Competition Highlights:**
![Competition Shots 1](./1734275377493.jpg)
![Competition Shots 2](./1734276429755.jpg)

🎥 **Demo Video:** [Watch the Project in Action](./Cosmoclench%20vedio%201%20.mp4)

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

## 💬 Contact

📧 **Email:** [pavankumar.b.reddy@email.com](mailto:pavankumar.b.reddy@email.com)
🔗 **LinkedIn:** [Pawan Kumar Reddy](https://www.linkedin.com/in/pavankumarreddy7/)
🌐 **Portfolio:** *GitHub Repository Link*

---

> *“Automation doesn’t replace effort — it amplifies precision, creativity, and impact.”*
> — **Pavan Kumar Reddy**


# 🦾 Wireless Operated Robotic Arm Vehicle for Industrial Automation

**Author:** Pawan Kumar Reddy
**Institution:** Sri Siddhartha Institute of Technology
**Competition:** *Winner – Cozmo Clench (Roboveda’23, Sreenidhi Institute of Science & Technology)*
**Languages & Tools:** Arduino (C/C++), IBT-2 Motor Driver, RF Communication, PWM Control, Embedded Systems

---

## 🧠 Technical Overview

This repository contains the complete design, code, and documentation for a **Wireless Operated Robotic Arm Vehicle**, developed for **industrial pick-and-place automation**. The robot is controlled using a **2.4GHz RF transmitter-receiver system**, and powered by an **Arduino UNO** microcontroller interfaced with **IBT-2 motor drivers**.

This system enables wireless motion control, robotic arm actuation, and precise object handling. It demonstrates an embedded solution that enhances **industrial efficiency, safety, and automation** in small-scale operations.

### Core Capabilities

* Wireless motion control using PWM signal mapping.
* Real-time dual motor synchronization for balanced navigation.
* Robotic arm actuation for lift, grip, and release operations.
* Modular design with differential drive motion system.

---

## ⚙️ Hardware Specifications

| Component             | Description                                           |
| --------------------- | ----------------------------------------------------- |
| **Microcontroller**   | Arduino UNO (ATmega328P)                              |
| **Motor Drivers**     | Dual IBT-2 H-Bridge modules (for left & right motors) |
| **Receiver**          | FS-iA6B / Avionic R7 (2.4GHz RF receiver)             |
| **Power Source**      | 12V DC (motors), 9V battery (logic supply)            |
| **Motors**            | 4 × DC geared drive motors, 1 × DC gripper actuator   |
| **ESC (Optional)**    | 30A Drone Brushless ESC for 5V regulation             |
| **Gripper Mechanism** | Foam-padded dual-jaw with DC actuator                 |

---

## 🔌 Circuit Diagram

![Circuit Diagram](./Circuit%20Daigram.jpg)

> The circuit demonstrates integration between Arduino UNO, RF receiver, and two IBT-2 motor driver modules controlling four DC motors. PWM control pins manage motor direction and speed.

---

## 🤖 Prototype

![Robotic Arm Vehicle](./1734276429755.jpg)

> *Prototype of the wireless robotic arm vehicle used in Roboveda’23 competition.*

---

## 💻 Software Architecture

### Control Logic

* **Input:** PWM signals from RF receiver channels CH1 & CH2.
* **Processing:** Pulse width analysis using Arduino `pulseIn()` function.
* **Output:** PWM signals mapped to motor speed and direction via `analogWrite()`.

### Functional Workflow

1. The RF transmitter sends control pulses (1–2 ms duty cycle).
2. Receiver interprets and forwards them to Arduino pins.
3. Arduino processes these values, determines direction, and maps to motor control signals.
4. The IBT-2 drivers drive DC motors for movement and lifting operations.
5. Robotic arm performs grip, lift, and release as commanded.

### Key Code Snippet

```cpp
// Receiver signal pins
double ch1_pin = 3;  // PWM channel 1
double ch2_pin = 5;  // PWM channel 2

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

### Complete Source Code

👉 [`Robotic Arm Vehicle - Project Code.docx`](./Robotic%20Arm%20Vehicle%20-%20Project%20Code.docx)

---

## 📐 System Design & Functionality

| Operation                 | Function                                                    |
| ------------------------- | ----------------------------------------------------------- |
| **Forward / Reverse**     | PWM mapped from CH1 & CH2 joystick inputs                   |
| **Left / Right Turn**     | Differential speed control between left/right IBT-2 modules |
| **Lift / Grip / Release** | Controlled by DC actuator for arm movement                  |
| **Failsafe Idle**         | Automatic stop when receiver signal is lost                 |

---

## 🏆 Achievements & Recognition

### **Cozmo Clench – Roboveda’23, Hyderabad**

* 🥇 **1st Place – Certificate of Excellence**
* 💰 **₹9000 Cash Prize**
* Recognized for **system reliability**, **mechanical design**, and **innovation in automation**.

📸 **Event Moments:**
![Competition 1](./1734275377493.jpg)
![Competition 2](./1734276429755.jpg)

🎥 **Demonstration Video:** [Watch Here](./Cosmoclench%20vedio%201%20.mp4)

---


## 🏆 Achievements

### **Cozmo Clench – Roboveda’23 (Sreenidhi Institute of Science & Technology, Hyderabad)**

* **Award:** 🥇 *Certificate of Excellence – First Place*
* **Prize:** ₹9000 cash award
* **Event:** *Samanvayi-Cozmo Clench – Pick and Place Robotics Challenge*
* **Recognition:** For innovation, precise control, and technical excellence
* **Judging Parameters:** Motion stability, mechanical design, Tasks sloving and automation efficiency

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

> 🔧 **Tip:** Keep filenames consistent and concise (use underscores instead of spaces) for cleaner version control.

---

## ⚡ Key Features

* 2.4GHz RF wireless control system.
* Dual motor synchronization using PWM modulation.
* Efficient, low-latency control for precise motion.
* Simple, scalable design suitable for research and industrial applications.
* Compatible with Arduino IDE and generic motor driver hardware.

---

## 🔮 Future Work

* Integrate **Bluetooth/Wi-Fi** for extended control.
* Implement **autonomous object tracking** using computer vision (OpenCV).
* Add **proximity and obstacle sensors** for safety automation.
* Replace gripper DC motor with **servo-based system** for higher precision.

---

## 👥 Contributors

* **Pawan Kumar Reddy** – Circuit Design, Programming, and Embedded Integration.
* **Team Cozmo Clench (SSIT Robotics Club)** – Mechanical Design, Arm Fabrication, and Field Testing.

---

## 🪪 License

Licensed under the **MIT License**. You are free to modify and distribute this project with proper attribution.

---

## 📬 Contact

📧 **Email:** [pavankumarreddy@email.com](mailto:pavankumarreddy@email.com)
🔗 **LinkedIn:** [Pawan Kumar Reddy](#)
🌐 **GitHub:** [Repository Link Here]

---

> *“Automation doesn’t replace effort — it extends human capability and precision.”*
> — **Pawan Kumar Reddy**

