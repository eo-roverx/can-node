# CAN Node PCB Designs

Part of the new arm system, wherein each PCB drives one motor, provides it feedback control, and (if needed) gives back IMU and encoder data. Our CAN node will have the following features:

- CAN bus communication
- IMU (accelerometer, gyroscope)
- Motor encoder input
- Motor driver
- 4 user defined LEDs + one status LED
- 4 bit address DIP switch
- ESP32 microcontroller: integration and feedback control

## Components
- ESP32 Microcontroller
- MPU9250 IMU
- MCP2551 CAN Transceiver
- 2x CAN RJ45 ports
- 2x XT60 solder pads for power
- MD13 Motor Driver
- MD13 power XT60 solder pads
- MD13 signal JST
- motor encoder JST
- 5V buck converter
- I2C pull-up resistors
- CAN termination resistor solder pads
- I2C debug solder pads
- CAN Rx-Tx debug solder pads
- 4x dip switch
- 1 power LED
- 1 status LED
- 4 user defined LEDs
    - 2 used for CRx-CTx

## ESP32 Pin-out

### CAN Bus
-  D2 CAN Rx
- D15 CAN Tx

### IMU
- D21 SDA
- D22 SCL
- D18 FSYNC
- D19 INT

### Motor encoder
- D34 pin A
- D33 pin B

### MD13 Motor Driver
- D26 PWM
- D25 DIR

### LEDs
- D32 status
- D13 user 0 (all nodes are connected)
- D12 user 1 (CAN Rx)
- D14 user 2 (CAN Tx)
- D27 user 3 (MPU calibration)

### Address DIP switches
- D4 address 0
- RX2 address 1
- TX2 address 2
- D5 address 3