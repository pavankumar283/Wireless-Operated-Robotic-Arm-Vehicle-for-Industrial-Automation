# Wireless-Operated-Robotic-Arm-Vehicle-for-Industrial-Automation
This system is very beneficial for places where there is a need to pick an object move it and place it to some other place safely. If the object is being picked by a human, there is a risk of damage to the object which is avoided by this system.


# 🦾 Wireless Operated Robotic Arm Vehicle for Industrial Automation

**Author:** Pawan Kumar Reddy
**Institution:** Sri Siddhartha Institute of Technology
**Competition:** *Winner – Cozmo Clench (Roboveda’23, Sreenidhi Institute of Science & Technology)*
**Language & Tools:** Arduino (C/C++), IBT-2 Motor Driver, 8051 Microcontroller Concept, RF Communication

---

## 🧠 Project Overview

This project presents a **Wireless Operated Robotic Arm Vehicle** designed for **industrial automation and remote pick-and-place applications**. The system integrates a **robotic arm** mounted on a mobile vehicle, controlled wirelessly via an **RF transmitter-receiver module (FS-iA6B/Avionic R7 2.4GHz)**.

The prototype was developed with **Arduino UNO**, **IBT-2 dual motor drivers**, and a **12V DC power source**, demonstrating how automation can **increase handling efficiency by 30%** compared to manual labor in small-scale industries.

The robot performs the following key operations:

* Remote **movement** (forward, backward, left, right)
* Controlled **arm lift, grip, and release**
* Precision **object handling** across varied surfaces

---

## ⚙️ Hardware Components

| Component                             | Description                                                  |
| ------------------------------------- | ------------------------------------------------------------ |
| **Microcontroller**                   | Arduino UNO (ATmega328P)                                     |
| **Motor Drivers**                     | 2 × IBT-2 H-Bridge Dual Drivers                              |
| **Receiver Module**                   | FS-iA6B / Avionic R7 2.4GHz                                  |
| **Power Supply**                      | 12V Battery + 9V for logic power                             |
| **Motors**                            | 4 DC geared motors for wheels + 1 DC arm actuator            |
| **ESC (Electronic Speed Controller)** | 30A Brushless Drone ESC (optional for 5V regulation)         |
| **Arm Mechanism**                     | Custom-built gripper with foam pads for safe object handling |

---

## 🔌 Circuit Diagram

![Circuit Diagram](./Circuit%20Daigram.jpg)

> The circuit connects two IBT-2 motor driver modules to control the left and right wheels, with PWM signals from the Arduino. The receiver channels CH1 and CH2 manage forward/reverse and turning motions.

---

---

## 🔌 Robotic Arm Vehicle Photo

![BOT Photo](C:\Users\bpava\OneDrive\Documents\College_Projects\1734276429755.jpg)

> The circuit connects two IBT-2 motor driver modules to control the left and right wheels, with PWM signals from the Arduino. The receiver channels CH1 and CH2 manage forward/reverse and turning motions.

---
## 💻 Arduino Code

Full Arduino implementation is available in:
[`Robotic Arm Vehicle - Project Code.docx`](./Robotic%20Arm%20Vehicle%20-%20Project%20Code.docx)

**Main Functions:**

* Reads PWM signals from receiver channels (CH1, CH2)
* Maps input to motor speed and direction (FWD, BACK, LEFT, RIGHT)
* Drives both motor drivers synchronously for precise movement
* Supports bidirectional motion and failsafe idle state

Key snippet:

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

1. The transmitter sends control signals via RF (2.4 GHz).
2. The receiver decodes these into PWM pulses fed to Arduino.
3. The Arduino interprets pulse width (typically 1000–2000 µs) to determine direction and speed.
4. Based on input range thresholds, PWM signals are sent to the motor drivers.
5. The robotic arm performs lifting, gripping, and releasing actions precisely as commanded.

---

## 🏆 Achievements

### **Cozmo Clench Competition (Roboveda’23 – Sreenidhi Institute of Science & Technology, Hyderabad)**

* **Event:** *Samanvayi & Cozmo Clench – Pick and Place Robotics Challenge*
* **Award:** *Certificate of Excellence – First Place Winner* 🥇
* **Prize:** ₹9000 Cash
* **Recognition:** For exceptional problem-solving, innovation, and system design
* **Judged on:** Robotic precision, structural stability, and speed of operation

📸 **Event Highlights:**
![Competition Moments](./1734275377493.jpg)
![Team Photo](./1734276429755.jpg)

🎥 **Demo Video:** [Competition Performance](./Cosmoclench%20vedio%201%20.mp4)

---

## 📁 Recommended Repository Structure

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

> 🔧 **Tip:** Rename all files using snake_case or PascalCase for clean readability.
> Example: `Robotic_Arm_Vehicle_Code.ino` instead of `Robotic Arm Vehicle - Project Code.docx`.

---

## 🚀 Key Features

* RF-based wireless operation
* Dual-axis motion control with differential drive
* Efficient arm actuation for pick-and-place tasks
* Lightweight and modular mechanical design
* Cost-effective prototype for small industries

---

## 🔮 Future Improvements

* Replace RF with **Bluetooth or Wi-Fi** for extended range
* Add **ultrasonic sensors** for obstacle avoidance
* Introduce **autonomous mode** using machine vision
* Upgrade gripper for variable-sized object handling

---

## 🪪 License

This project is licensed under the **MIT License** – feel free to use, modify, and distribute with attribution.

---

## 💬 Contact

For collaboration or inquiries:
📧 **Email:** [[pavankumarreddy@email.com](mailto:pavankumarreddy@email.com)]
🔗 **LinkedIn:** [Pawan Kumar Reddy](#)
🌐 **Portfolio:** [GitHub Repository Link Here]

---

> *“Automation doesn’t just replace effort — it amplifies precision, speed, and imagination.”*
> — *Pawan Kumar Reddy*
