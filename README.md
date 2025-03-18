# ESP32 Air Mouse with MPU6050 & Bluetooth HID

🚀 Turn your ESP32 into a Wireless Air Mouse!
Move the cursor by tilting your hand, click with an FSR or button, and scroll using gestures.

---

## 🎯 Features

✅ **Motion Control:** Move the mouse by tilting your hand (MPU6050).  
✅ **Left Click:** Press an FSR (Force Sensor) or a button (GPIO 32).  
✅ **Right Click:** Press a button (GPIO 33).  
✅ **Scrolling:**  
- **Method 1:** Tilt hand forward/backward.  
- **Method 2:** Press a button (GPIO 34).  
✅ **Wireless Bluetooth HID:** No PC script needed—connects as a real Bluetooth mouse!  

---

## 📦 Hardware Required

| Component       | Quantity |
|----------------|----------|
| ESP32 Board    | 1        |
| MPU6050 IMU Sensor | 1    |
| FSR (Force Sensitive Resistor) or Button | 1 |
| Push Buttons   | 2        |
| Resistors (10kΩ) | 3      |
| Breadboard & Jumper Wires | As needed |
| Battery (For wireless use) | 1 |

---

## 📌 Pin Configuration

| Component  | ESP32 GPIO Pin |
|------------|---------------|
| MPU6050 VCC | 3.3V |
| MPU6050 GND | GND  |
| MPU6050 SDA | GPIO 21 |
| MPU6050 SCL | GPIO 22 |
| Left Click (FSR/Button) | GPIO 32 |
| Right Click Button | GPIO 33 |

---

## 🔧 Setup & Installation

### 1️⃣ Install Arduino Libraries

- **MPU6050** (`arduino-mpu6050`)
- **NimBLE-Arduino** (`NimBLEDevice`)

### 2️⃣ Upload Code to ESP32

- Select ESP32 board in Arduino IDE.
- Connect ESP32 via USB and upload the code.

### 3️⃣ Connect Bluetooth on PC/Phone

- Go to Bluetooth Settings → Add a new device.
- Select **"ESP32 AirMouse"** from the list.
- Pair and start using the air mouse!

---

## 📜 Code Explanation

1️⃣ Reads motion data from MPU6050.  
2️⃣ Converts gyroscope values into mouse movements.  
3️⃣ Detects button presses for left/right click.  
4️⃣ Sends HID mouse commands over Bluetooth.  

---

## 🛠️ Troubleshooting

🔹 **Bluetooth not connecting?**  
🔸 Restart ESP32 and try pairing again.  
🔸 Remove **"ESP32 AirMouse"** from Bluetooth devices and re-add.  

🔹 **Mouse movement too fast/slow?**  
🔸 Adjust `map(gx, -20000, 20000, -5, 5);` in the code.  

🔹 **Click not working?**  
🔸 Check wiring of FSR/button to GPIO 32 & 33.  


