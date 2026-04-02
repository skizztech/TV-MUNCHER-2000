# TV-MUNCHER-2000
This project is a high-power infrared (IR) transmitter designed to control TVs at extended range. It uses a MOSFET to switch a high-output IR LED, allowing significantly higher current and stronger signal output than standard remotes.

The system is powered by a rechargeable battery and includes a boost converter to maintain a stable voltage. A microcontroller generates the IR signal patterns, which are emitted in short, high-intensity bursts.

Overall, the design focuses on maximizing IR output power and range while keeping the system compact and efficient.

## Parts List

- Arduino Nano
- IRLZ44NPBF MOSFET (logic-level N-channel)
- 10kΩ Resistor (pull-down for MOSFET gate)
- Chanzon 10W 940nm IR LED
- 6x6mm Tactile Push Button

WIRE BEFORE FLASHING THE CODE
  
wire scheme

IMPORTANT!!!! you must share one gnd pin on the arduino or it will not work
## Wiring

- **Tactile Button**
  - Pin 1 → GND (Arduino)
  - Pin 2 → D2 (Arduino)

- **IR LED**
  - Positive (+) → 5V (Arduino)
  - Negative (−) → MOSFET Drain (middle pin)

- **MOSFET (e.g. IRLZ44N)**
  - Gate (left pin) → D3 (Arduino)
  - Drain (middle pin) → IR LED negative (−)
  - Source (right pin) → GND (Arduino)

- **10kΩ Resistor (Pull-down)**
  - One side → GND (Arduino)
  - Other side → MOSFET Gate (left pin)
    
![20240828124104515](https://github.com/user-attachments/assets/7405eb24-babd-4f72-8b04-7405f63e760b)
<img width="595" height="422.5" alt="SCH_Schematic1_1-P1_2026-04-02" src="https://github.com/user-attachments/assets/52cab201-8270-43c3-bbc7-73756f7ac4bd" />

FLASHING THE CODE TO THE ARDUINO

## Setup Instructions

1. Go to **Releases** and download `Arduino-TV-B-Gone-1.3.zip`.

2. Open the **Arduino IDE** and connect your **Arduino Nano** to your computer.

3. In Arduino IDE:
   - Go to **Tools → Board → Arduino Nano**
   - Select the correct **COM Port**

4. Install the library:
   - Go to **Sketch → Include Library → Add .ZIP Library**
   - Select `Arduino-TV-B-Gone-1.3.zip`
   - Click **OK** and wait for it to install

5. Close the Arduino IDE.

6. Extract the ZIP file:
   - Locate `Arduino-TV-B-Gone-1.3.zip`
   - Extract it
   - Open the extracted folder
   - Keep clicking through folders until you find:
     - `Arduino_TV_B_Gone.ino`

7. Double-click the `.ino` file to open it in Arduino IDE.

8. Reconnect/select your board:
   - **Tools → Board → Arduino Nano**
   - Select your **COM Port**

9. Upload the code:
   - Click **Sketch → Upload** (or press the upload button)

10. Once uploaded:
    - Press the button on your device
    - It will transmit the TV-B-Gone IR signal
