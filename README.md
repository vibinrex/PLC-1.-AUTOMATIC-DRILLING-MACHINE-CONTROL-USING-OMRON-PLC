# PLC-1.-AUTOMATIC-DRILLING-MACHINE-CONTROL-USING-OMRON-PLC

## Aim
To design and implement an Automatic Drilling Machine Control System using an Omron PLC.

## Objective
1.	To understand PLC/. -based sequence control.
2.	To control forward and reverse operation of a drilling motor.
3.	To use limit sensors for automatic positioning.
4.	To implement emergency stop functionality.

## Apparatus Required
•	Omron PLC (CP1E/CP1L)
•	CX-Programmer Software

## Theory
Automatic drilling machines are widely used in manufacturing industries. The drill moves downward to perform the drilling operation and returns upward automatically after reaching the required depth. PLC controls the motor direction using forward and reverse commands based on sensor feedback.

## Procedure
1.	Open CX-Programmer.
2.	Create a new Omron PLC project.
3.	Configure the I/O addresses.
4.	Develop the ladder logic.
5.	Download the program to the PLC.
6.	Switch PLC to RUN mode.
7.	Press START PB.
8.	Observe downward drilling operation.
9.	Observe automatic reversal at the bottom sensor.
10.	Observe stopping at the upper sensor.
11.	Press STOP PB and verify immediate stopping.

## I/O Address Assignment

## Inputs
Device	Description	Address
Start PB	Start Push Button	0.00
Stop PB	Stop Push Button	0.01
Drill Up Sensor	Home Position Sensor	0.02
Drill Down Sensor	Bottom Position Sensor	0.03

## Outputs
Device	Description	Address
Forward Motor	Drill Down Movement	100.00
Reverse Motor	Drill Up Movement	100.01

## Internal Relay
Function	Address
Machine Run Bit	W0.00


## Sequence Diagram
             START PB
                 |
                 V
        Forward Motor ON
                 |
                 V
       Drill Moving Down
                 |
                 V
      Drill Down Sensor ON
                 |
                 V
        Reverse Motor ON
                 |
                 V
        Drill Moving Up
                 |
                 V
       Drill Up Sensor ON
                 |
                 V
          Motor STOP



## Output


















## Result
The Automatic Drilling Machine Control System was successfully implemented using an Omron PLC. The drill moved downward in the forward direction, reversed automatically upon reaching the bottom position, returned to the home position, and stopped safely. The Stop Push Button provided immediate shutdown during operation.
