[M4x10 screws]:Parts.yaml#M4x10PanSteel
[No. 2 Phillips screwdriver]:Parts.yaml#Screwdriver_Philips_No2

# Control Board Specifications

{{BOM}}

# Overview
This board collects all the signals from the charging and discharging board and carry out all the downstream processing on the collected data. It sends control signals to the (dis)charge boards that set the charging current as well as controlling the switch between charging and discharging states. This board also communicate with the I/O board.

# Features
* Micro-controller with Bluetooth communication with the App
* Programmable charging current to all the boards
* Multiplexed reading of voltage and current measurements from (dis)charging boards
* Simultaneous setting of charging and switching states

## Power supply
* VDD +5V
* Ground

# Functional block diagram

![](images/control1001.png)

# Components
This section describes all the Integrated Circuit (IC) components that are on the control circuit board.
Due to limitations in the number of I/O pins on the pico, multiplexers and shift registers are used to send and read signals from the 8 charging/discharging board instead of direct connection from board to pico.

**Raspberry Pi Pico W**


**Multiplexer (MUX)**
The two MUX read voltage and current measurements respectively from the 8 battery boards. They need to read analog voltages between 0 and 5V. Three control lines are used to select which channel to read. Note, the two mux share the same control lines, hence the two measurements from each battery board need to be wired to the same channel on the two mux.

**Shift Registers**
The two shift registers control the charging/discharging switches on the battery boards. A series of 16 bit logic (which 8 for charging and 8 for discharging) is sent from pico to the shift registers, on the rising edge of the register clock, the register presents the logic at the 16 outputs and holding it until it is cleared. 

**Digital to analog converter (DAC)**
The DAC allows the programmable charging current function in this device. The SPI communication is set up between the pico and the DAC, the DAC converts the digital command from the pico into an analog voltage, which is then sent to all the battery boards to be converted to the specified current.

**Op-Amp**
The op-amps scale the voltage and current measurements from the battery board from 0-5V to 0-3.3V, which is the input voltage range of the pico. The firmware specifies which mux channel to read out, and that read out is down scaled before input into the ADC on the pico.
Resistors are matched within 1% for accurate readouts.
Hardware Interfaces
This section describes the interfaces the control board with the other circuit boards in the system and list the input and output pins from the perspective of the control board.

**Power board**
Vcc +5V
Ground
Max T – temperature pin from the power board, which is the voltage recorded by the temperature sensor on the (dis)charge board with the highest temperature

**I/O board**
5 pin connector that interfaces with the SD card module
3 pin connector which 2 lines for I2C communication with the LCD screen, and 1 carries the ambient temperature from the I/O board into one of the ADC within the pico. 
4 pin connector that carries signal from the rotary encoder (2 lines) and the button (2 lines).

**(Dis)charge boards (each)**
2 input pins – one for the voltage measurement and one for the current measurement
3 output pins – one for setting the charging current, 2 for the switching signals to the relays that switch the charging and discharging modes.





