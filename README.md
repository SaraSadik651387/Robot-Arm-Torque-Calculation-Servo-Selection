# 📌 Robot Arm Torque Calculation & Servo Selection

## 📖 Overview
This project involves calculating the **torque** required for each joint in a robotic arm and selecting the appropriate **servo motors** based on the computed torque values.

The robotic arm has **three joints**, and each segment has a specific length:
- **Joint 1:** 4 cm
- **Joint 2:** 10 cm
- **Joint 3:** 15 cm
- **End Effector Load:** 1 kg

---

## 🔢 **Torque Calculation Formula**
Torque (𝜏) is calculated using the formula:

\[
\tau = r \times F
\]

Where:
- **\( \tau \)** = Torque (N·cm)
- **\( r \)** = Length of the arm segment (cm)
- **\( F \)** = Force applied due to the load (N), calculated as:

\[
F = m \times g
\]

With:
- **\( m \)** = 1 kg (Mass of the object)
- **\( g \)** = 9.81 m/s² (Acceleration due to gravity)

---

## 🧮 **Torque Calculations for Each Joint**
| Joint | Length (cm) | Force (N) | Torque (N·cm) |
|--------|------------|------------|----------------|
| **Joint 1** | 4 cm | 9.81 N | **39.24 N·cm** |
| **Joint 2** | 10 cm | 9.81 N | **98.10 N·cm** |
| **Joint 3** | 15 cm | 9.81 N | **147.15 N·cm** |

---

## 🛠 **Selected Servo Motors**
After calculating the required torque, servo motors were selected based on their torque ratings.

| Joint | Required Torque | Selected Servo | Max Torque | Purchase Link |
|--------|----------------|--------------------|------------|---------------|
| **Joint 1 (4 cm)** | **39.24 N·cm** | **Tower Pro MG996R** | **107.9 N·cm** | [Buy Here](https://www.amazon.sa/%D9%85%D8%AD%D8%B1%D9%83-%D8%B3%D9%8A%D8%B1%D9%81%D9%88-MG996R-%D8%AA%D8%A7%D9%88%D8%B1-%D8%A8%D8%B1%D9%88/dp/B00MTGV3TA) |
| **Joint 2 (10 cm)** | **98.10 N·cm** | **FEETECH Brushless Servo** | **300 N·cm** | [Buy Here](https://www.amazon.sa/-/en/FEETECH-Aluminum-Brushless-Rotation-Steering/dp/B097DGT8G7?th=1) |
| **Joint 3 (15 cm)** | **147.15 N·cm** | **High Torque 180Kg·cm Servo** | **1765 N·cm** | [Buy Here](https://ardunic.com/product/High-Torque-Servo-12-24V-180KgCm-Steel-Gear) |

---

## 🔍 **Key Considerations for Servo Selection**
1. **Torque Buffer**: Chose servos with torque **20-30% higher** than the required torque to ensure stability.
2. **Voltage Compatibility**: Ensure servos operate within the **microcontroller’s voltage range**.
3. **Physical Fit**: The selected servos should fit within the **robot arm’s structure**.

---

### 🚀 **Next Steps**
- Implement the servo motors into the robotic arm.
- Write an **Arduino control code** to move the arm.
- Optimize power supply requirements for smooth operation.

