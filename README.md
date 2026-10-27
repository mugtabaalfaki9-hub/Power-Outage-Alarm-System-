buttonPinttonPinPower Outage Alarm System

![Arduino](https://img.shields.io/badge/Arduino-Uno-blue)
![Tinkercad](https://img.shields.io/badge/Simulated_on-Tinkercad-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

📝 Overview
This is a prototype to provide an immediate alert during a power outage, simulated using Tinkercad where a pushbutton simulates outage and triggers Piezo buzzer.

🎯 Problem & Solution
**The Problem:** In Sudan, frequent power outages risk damaging appliances (Voltage Surges).
**The Solution:** Low-cost alarm that notifies user to disconnect appliances.

🛠️ Components Used
* Arduino Uno R3, Pushbutton, Piezo Buzzer, 10kΩ Resistor, Breadboard


## 💻 Source Code
```cpp
int buttonPin = 2;
int buzzerPin = 3;
void setup() {
  pinMode(buttonPin, INPUT);
  pinMode(buzzerPin, OUTPUT);
}
void loop() {  if (digitalRead(buttonPin) == HIGH) tone(buzzerPin, 1000);
  else noTone(buzzerPin);
}
```
⚙️ How it works
1. Normal: LOW, buzzer silent
2. Outage: HIGH, buzzer at 1000Hz
3. Restored: LOW, stops

🚀 Live Simulation
**[Click here to try Live Simulation](https://www.tinkercad.com/things/9leJTsCdcSo-power-outage-alarm)**

🔮 Future Improvements
- Replace button with AC Voltage Sensor
- Add Relay for Emergency Light
- Add GSM SIM800L for SMS alerts
