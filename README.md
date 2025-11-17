# Anti-Theft Alert System using Tilt Sensor

## Aim

To measure the **Tilt Sensor (SW200D)** using **Arduino UNO Board / ESP-32** in **Tinkercad**.

---

## Hardware / Software Tools Required

* PC / Laptop with Internet connection
* Tinkercad (Online Simulation Tool)
* Arduino UNO Board / ESP-32
* Tilt Sensor (SW200D)

---

## Circuit Diagram
---

<img width="1919" height="993" alt="image" src="https://github.com/user-attachments/assets/2c09c488-5e39-4e1d-989b-96ae6dfdee50" />

---

## Theory

The **Arduino Uno** is powered by the **ATmega328P**, an 8-bit microcontroller that runs at **16 MHz**. It includes:

* **Memory:** 32 KB of Flash, 2 KB of SRAM, and 1 KB of EEPROM
* **I/O Pins:** 14 digital I/O pins (6 PWM-capable) and 6 analog input pins
* **Power Supply:** Can be powered via USB or an external source (7–12V) with a built-in voltage regulator
* **Programming:** The Arduino IDE (Integrated Development Environment) uses a simplified version of C/C++, and the uploaded program is known as a *sketch*.
* **Communication:** The Uno has a USB-B port used for programming and power supply via computer connection.
* **Additional Features:**

  * Reset button for restarting the microcontroller during testing or programming
  * ICSP header for low-level programming and firmware updates
  * Built-in LED on pin 13 for simple debugging or testing

The **SW200D Tilt Sensor** detects changes in angular position or movement. It works by completing or breaking an electrical circuit when tilted, making it useful for **anti-theft systems**, **motion detection**, and **orientation-based projects**.

---

## Procedure

### Step 1: Set Up the Tinkercad Environment

1. **Log in to Tinkercad:** Open Tinkercad in your web browser and sign in to your account.
2. **Create a New Circuit:** In the dashboard, go to **Circuits** → **Create New Circuit**.

---

### Step 2: Add Components to the Circuit

* **Arduino Uno:** Drag and drop an Arduino Uno board into the workspace.
* **SW200D Sensor:** Search and add the SW200D tilt sensor.
* **Breadboard:** Add a small breadboard for organizing connections.
* **Resistor (Optional):** May be added for stable readings.
* **Jumper Wires:** Use wires to connect all components properly.

---

### Step 3: Connect the Tilt Sensor (SW200D) to Arduino

* **SW200D Vout (Middle Pin):** Connect to Arduino **Digital Pin D2**.
* **SW200D GND (One Side Pin):** Connect to the **Ground (GND)** rail of the breadboard.
* **SW200D VCC (Other Side Pin):** Connect to the **5V rail** of the breadboard.

---

### Step 4: Write the Arduino Code

1. Click on the **Code** button in the Tinkercad workspace.
2. Switch to **Text Mode** to write your program in C/C++.
3. Enter the appropriate code for the **SW200D Tilt Sensor** to read its state and trigger an alert when tilted.

---

### Step 5: Simulate the Circuit

* Click **Start Simulation** at the top of the workspace to run your project.
* Use the **Serial Monitor** to observe the tilt sensor’s readings and behavior.

---

### Step 6: Troubleshoot and Refine

* Verify all **connections** on the breadboard and Arduino.
* Adjust the **code logic** or delay times for improved sensor response or alert accuracy.

---

### Step 7: Save Your Work

* Click **Stop Simulation** once testing is complete.
* Click **Save** to preserve your circuit design and code for future use.

---

## Code

```c
int ledPin=13;
int inPin=7;
void setup()
{
 Serial.begin(9600);
  pinMode(ledPin,OUTPUT);
  pinMode(inPin,INPUT);
}
void loop()
{
  int val=digitalRead(inPin);
  if(val==0)
  {
    digitalWrite(ledPin,HIGH);
  }
  else
  {
    digitalWrite(ledPin,LOW);
  }
}
```

---

## Output

---

<img width="1919" height="998" alt="image" src="https://github.com/user-attachments/assets/065e1d7c-b98b-4be0-ad20-4bbdcabb199e" />

---

## Result
Thus, the Tilt Sensor (SW200D) interfaced with the **Arduino UNO Board / ESP-32** using **Tinkercad** has been successfully simulated and verified for the **Anti-Theft Alert System** application.
