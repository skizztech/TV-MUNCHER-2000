# TV-MUNCHER-2000
This project is a high-power infrared (IR) transmitter designed to control TVs at extended range. It uses a MOSFET to switch a high-output IR LED, allowing significantly higher current and stronger signal output than standard remotes.

The system is powered by a rechargeable battery and includes a boost converter to maintain a stable voltage. A microcontroller generates the IR signal patterns, which are emitted in short, high-intensity bursts.

Overall, the design focuses on maximizing IR output power and range while keeping the system compact and efficient.

PARTS LIST
-Arduino Nano
-irlz44nPBF mosfet
-10k ohm resistor
-Chanzon 10w 900mah 940nm led
-tactile 6x6 button

wire scheme

IMPORTANT!!!! you must share one gnd pin on the arduino or it will not work

tactile button 1pin to gnd on arduino and 2nd pin to D2 on arduino
ir led negetive to mosfet middle pin(drain)
ir ed positive to arduino 5v
mosfet left pin(gate) to D3 on arduino and 10k ohm resistor one pin on gnd and the other on the mosfet left pin
mosfet right pin(source) to gnd on arduino

![20240828124104515](https://github.com/user-attachments/assets/7405eb24-babd-4f72-8b04-7405f63e760b)


optional coming soon
BATTERY
