# Day 1 – Furuta Pendulum

## 1. Topics Covered:
- What is a microcontroller?
- What are sensors?
- What is communication?
- What is a communication bus?
- Types of communication: UART, SPI and I2C
- Why does our project use I2C?

## 2. Concepts I Learned
I understood that Arduino UNO contains the microcontroller "ATMEGA328p). A microcontroller is a small programmable computer tha reads inputs from sensors, process infos and controls output devices. 
Some of the sensors that I came to know were:
- Ultrasonic sensors (HC-SR04)
- Temperature sensor
- IMU (measures accelerationa and angular velocity)
- Rotary encoder (measures rotational position or movement)

  Arduino -> IMU->Motor driver connected to motors
  The main learning was how does the communication happen between Arduino and IMU (Through electrical signals)

  Communication Buses are roads that helps electronic components (buildings) exchange data (vehicles).

  These roads have different communication protocols some them that I learnt were:
  1) UART (Universal unsynchronous reciever transmitter)
  2) SPI (Serial peripheral interface
  3) I2C (Inter integrated circuit)
 
  In simple words, communication protocols are basically predefined rules for exchanging data.
  
  
## 3. Technical Notes
1) UART
It is a communication protocol that contains 2 communication lines TX and RX which stands for Transmite (Sending infos) and recieve (Recieving infos) respectively

2) SPI
It is another communication protocol that follows the master and slave concept.
Master refers to the one who asks for informations
Slave refers to the one who brings the information based on the request made by the Master

2 SPIs would connect based on:
MOSI -> MOSI [master out slave in]
MISO -> MISO [Master in slave out]
SCLK -> SCLK [Clock signal]
CS -> CS [Chip select]

3) I2C
This is a communication protocol that uses parallel connection between a master and the slave. Additionally it has the communication lines:
- SDA (Serial data)
- SCL (Serial clock)

## 5. Doubts and Challenges
As I was new to the whole topic, I faced some difficult in understanding how certain communication lines interact but today as I am starting new, I decided to learn it like a concept than to overlearn it.

## 6. What I Learned Today
Key takeaways:
- I learnt that IMU is a sensor
- I2C is a communication protocol and its not a physical component.
