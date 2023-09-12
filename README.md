# CRC_HARDWARE_IMPLEMENTATION

Cyclic redundancy check (CRC) is an error detection code commonly used in digital networks 
and storage devices to detect random changes to digital data. Data blocks entering these 
systems are assigned a short check value, based on the remainder of the polynomial division on 
their contents. On recovery, the calculation is repeated, and if the check values do not match, 
corrective action can be taken for data corruption.


## Features

- CRC can be used to correct errors.
- Easy to analyze mathematically.
- good at detecting common errors caused by noise in transmission channels.



## Block Diagram:

![block dia](https://github.com/Ismaeel53/CRC_HARDWARE_IMPLEMENTATION-/assets/127503048/0b425818-4b01-4d0b-aeec-f0084b676b83)

## Steps to make hardware design:
- Data transmission to 16 bit LED using Arduino Nano.
- Data transmission to receiver from transmitter 
- Making similar clock for transmitter and receiver
- CRC working 
- CRC calculation in hardware
## Data transmission to 16 bit LED using Arduino Nano:
First we place the Arduino Nano on bread board and hook up it’s digital pins with the 16 bit LED display 
screen and data pin is connected with a red led and display screen in order to see what data (0,1) is coming 
from the Arduino Nano.In this hardware Arduino Nano is used only for data and clock working which is on 
pin D3( data) and D2 (clock) . First we implement a simply code to see weather the 16 bit LED screen and 
red led is working or not then we move to the next step.So the data transfer to 16 bits display screen will 
look like this (some randome data): 

![Screenshot 2023-09-12 211814](https://github.com/Ismaeel53/CRC_HARDWARE_IMPLEMENTATION-/assets/127503048/d7991ef2-20cb-401d-980f-82d05b3b74ab)


## Data transmission to receiver from transmitter:
Receiver is made in same way we made the transmitter using Arduino Nano and connecting it to 
the 16 bit display screen and data pin of receiver is connected with display screen , green Led and 
with the transmitter data pin so data can be transfer from transmitter to receiver.both 
transmitter and receiver has common ground as well. Till this point the data is only transfer from 
transmitter to receiver but its not valid data transfer reason is that the receiver and transmitter 
has different clock beside same data pin connection we have to make both clock similar and after 
that we check weather the data is correct we start CRC implementation in next step.
## Making similar clock for transmitter and receiver:
To make clock similar we use d2 pin to transfer clock signal from transmitter to receiver and 
connect it with LED to see weather it is similar or not .From this there is three connection 
between transmitter and receiver ground ,data connection and clock signal connection.

![Screenshot 2023-09-12 212118](https://github.com/Ismaeel53/CRC_HARDWARE_IMPLEMENTATION-/assets/127503048/6f6aa4f2-e01c-42f7-b020-775605a4ad36)

## Simulation:

![Screenshot 2023-09-12 212649](https://github.com/Ismaeel53/CRC_HARDWARE_IMPLEMENTATION-/assets/127503048/72eae1cf-06fe-4f2e-8aeb-dd3786b59652)

## Hardware screenshot:

![Screenshot 2023-09-12 212911](https://github.com/Ismaeel53/CRC_HARDWARE_IMPLEMENTATION-/assets/127503048/65f06f06-0e77-4871-b68b-ec96b51ce3c0)   ![Screenshot 2023-09-12 213053](https://github.com/Ismaeel53/CRC_HARDWARE_IMPLEMENTATION-/assets/127503048/35e97366-18fd-43fc-82d1-016a451cb097)

![Screenshot 2023-09-12 212949](https://github.com/Ismaeel53/CRC_HARDWARE_IMPLEMENTATION-/assets/127503048/45a5b301-2ab4-4bb5-9bba-a390f484168d)
