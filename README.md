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
<img width="1190" height="845" alt="SCH_Schematic1_1-P1_2026-04-02" src="https://github.com/user-attachments/assets/52cab201-8270-43c3-bbc7-73756f7ac4bd" />


optional coming soon
BATTERY
