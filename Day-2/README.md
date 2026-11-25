# Day 2 – Furuta Pendulum

## 1. Topics Covered
- What is I2C?
- SDA and SCL pins.
- Master and slave.
- Device addresses
- How data travels between an IMU and microcontroller
- Understanding I2C wiring

## 2. Concepts I Learned
I2C - synchoronous serial communication protocol used to transfer data between electronic devices 
The term "Serial" refers to transferring data one but at a time.
I2C communicates between integrated circuits.

Masters - Initiates and controls communication 
Slave - Responds to the master

SDA -> SDA [Serial data line - carries the actual infos]
SLC -> SLC [Serial clock line - provides the timing for the communication of bits to be transferred]

In the project:
            Arduino UNO - Master
            MPU6050 IMU - Slave
I2C addresses are represented 0x68 (hexadecimal)

Where:
0x68 when its AD0 pin is LOW.
0x69 when its AD0 pin is HIGH.


## 3. Technical Notes
Working:
Arduino wants to read data from MPU6050 IMU
1) Arduino starts communication 
2) Arduino specifies the address (Ex: 0x68)
3) MPU6050 IMU recognises its address
4) MPU6050 IMU responds
5) Data is exchanged

I2C communication contains some keywords:
A.START condition
B.Address
C.ACK (Acknowledgment)
D. Data transfer
E.STOP condition           

Pull up resistors:
it is placed between device 1 and device 2
Device 1  -> Device 2 (SCL)
Device 1  -> Device 2 (SDA)     

When electronic device is connected to SCL, It pulls the line HIGH.
  
## 4. Practical Work
Arduino-IMU wiring:
3.3V/5V -> VCC
GND -> GND
A4 -> SDA
A5 -> SCL
D2 -> INT

where A4 and A5 are standard I2C pins on the Arduino UNO R3

## 5. Doubts and Challenges
I didn't find anything that difficult though understanding these concepts felt abstract at the start.

## 6. What I Learned Today
Key takeaway:
- I2C follows the master and slave method
- I2C calls upon its necessary sensors using addresses
- Pull up resistors are mandatory to ensure the line is pulled low with the help of a Resistor 1 and Resistor 2.
