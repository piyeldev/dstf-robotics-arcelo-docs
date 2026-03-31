The following are the parts used to create this robotics project, with explanations and other information. Some information might be vague or feature jargons, so google is your friend.
### 4x Blue DC Geared Motor 
![[Pasted image 20260326175604.png|456]]

This is the motor used to drive the robot in the 4 directions (forward, backward, left, right). This motor features a gearbox, which unlike a regular DC motor, has more strength or torque, which means it can carry more weight without stalling. This blue variant features metal gears, which are unlike the typical yellow hobby motors.

**Specifications:**
- Color: Blue  
- Operating Voltage: 3V to 6V DC  
- Gear Ratio: 1:90  
- Gear Material: All Metal Gears  
- Output Shaft Type: Single Shaft

### 2x Diaphragm Pump
![[Pasted image 20260326175710.png|466]]

This is a water pump, powered by a DC motor. It features two (2) holes, one for water in, and one for water out. The one in the robot was found inside an automatic water dispenser found in stores such as Grandiz, because these pumps were hard to find. We actually applied a higher voltage in these pumps, around 6-7V, as the operating voltage was too slow. This also came with drawbacks such as overheating, and loud noise.

**Specifications:**
- Voltage: 3-4.5V
- Current: 3V 650mA, 3.7V 750mA
- Power: 3-6W
- Lift: 1.5m
- Size: 80x31x24mm
- Import and export inner diameter: 4mm
- Import and export outer diameter: 7mm

### 2x 18650 3.7V Li-ion Battery
![[Pasted image 20260326175504.png|460]]

Used to power the robot overall. Unlike a regular AA battery, this battery is much larger and features a higher voltage (AA: 1.5V vs 18650: 3.7V), and a higher capacity, depending on the variant (in our case, 2200mAh). We used two batteries, and wired it in parallel to double the voltage, but kept the capacity the same.

**Specifications:**
- Battery Type: ICR 18650 3.7V 2200mAh Li-ion Rechargeable Battery  
- Model: ICR18650 3.7VLi-ion Battery  
- Voltage: 3.7V  
- Storage Voltage: 3.7-3.9V  
- Charging Cut-off Voltage: 4.2V  
- Discharge Cut-off Voltage: 3.0V  
- Capacity: 2200mAh  
- Size: 18.5x65.2mm  
- Protected: NO  
- Battery top: Flat top  
- Max Constant Charging Current: 2200mA(1C)  
- Max Constant Discharging Current: 4400mA(2C)  
- Material: Lithium Li-ion ICR  
- Recharging cycles: At least 500cycles

### 1x ESP32 C3-Supermini
![[Pasted image 20260326175804.png|461]]

This is the microcontroller that facilitates communications between phone and the robot. This board features WiFi and Bluetooth capabilities, meaning you can send and receive informations through those protocols. This also features pinouts (the one on the sides of the board), where you can send and receive information to and from hardware. To program this board, you need to use a USB type-C cable, and connect it to a computer or laptop with Arduino IDE.

**Specifications:**  
- Microcontroller: Espressif ESP32-C3 (RISC-V 32-bit single-core, up to 160 MHz)  
- Wireless Connectivity:  
	A. Wi-Fi: 802.11 b/g/n (2.4 GHz)  
	B. Bluetooth: Bluetooth Low Energy (BLE) 5.0  
- Flash Memory: 4MB  
- SRAM: 400 KB  
- Peripherals: Multiple GPIO pins (number varies by specific board, typically 22-30), ADC, DAC, I2C, SPI, UART, PWM, I2S, RMT, etc.  
- Power Input: 5V DC via USB-C port or VIN pin  
- Operating Voltage: 3.3V  
### 1x Arduino Uno R3
![[Pasted image 20260326175843.png|457]]

This is the main microcontroller that controls everything. This is slightly the same as the ESP32 in terms of capabilities, but it featues a bigger form factor, more pinouts (the blacks on the side), and more hardware capabilities. But unlike the ESP32, it doesn't feature any wireless connectivity, that's why we used an ESP32 together with it. To program this board, we use a USB type-B to type-A connector, and connect it to our computer that has Arduino IDE installed.

**Specifications:**
- Microcontroller: DIP ATmega328  
- Operating Voltage: 5V  
- Dual Inline Package  
- Input Voltage (recommended): 7-9V  
- Digital I/O Pins: 14 (of which 6 provide PWM output)  
- Analog Input Pins: 6  
- DC Current per I/O Pin: 40 mA  
- DC Current for 3.3V Pin: 50 mA  
- Flash Memory:32 KB (ATmega328) of which 0.5 KB used by the bootloader  
- SRAM: 2 KB (ATmega328)  
- EEPROM: 1 KB (ATmega328)  
- Clock Speed: 16 MHz

### 1x L293D Motor Driver Shield
![[Pasted image 20260326180019.png|455]]

This is the board that facilitates communication between Arduino and the motors, and regulates them. This board is inserted as a "shield" in the Arduino, like a sandwich. This board has also been known to be inefficient as the motors lose voltage, because of its old and unupdated design; but it does its work. It features four terminals (light blue left and right), for four motors or two terminals, for two stepper motors, and two terminals for two servos (in the upper left corner). 

**Features :**
- 2 interface for 5V Servo
- Can drive 4 DC motors or 2 stepper motors or 2 Servo
- Up to 4 bi-directional DC motors with individual 8-bit speed selection
- Up to 2 stepper motors (unipolar or bipolar) with single coil, double coil or interleaved stepping.
- 4 H-Bridges: per bridge provides 0.6A (1.2A peak current) with thermal protection, can run motors on 4.5V to 36V DC
- Pull down resistors keep motors disabled during power-up
- Reset button
- 2 external terminal power interface, for separate logic/motor supplies

### 2x F5305s Power MOSFET
![[Pasted image 20260326180537.png|454]]

This is the part that is used to switch the two diaphraghm pumps on or off. This works by using two terminals (+ and -), for controlling the on or off state, and another two terminals (+ and -), to supply electricity. This was used because the pump needed more voltage and current, more than what the microcontrollers can provide (microcontroller: 3V or 5V, needed: 6V-7V).

### 1x Red Water Sensor


### 1x Battery Holder

### 1x Rocker Switch
