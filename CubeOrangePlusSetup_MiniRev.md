# Main Steps for setting up connection to Cube Orange Plus

## Initial Connection

1. Connect Cube Orange+ Using Micro-B connector
2. Open Mission Planner
3. On the top right, change "COM" to Auto
4. Click Connect
    1. If Mission Planner displays an error, disconnect and reconnect the wire (power cycle) the cube orange from the USB connection on your computer

## Reciever (Rx) Setup (3 pin to 3 pin) and RTK Setup

1. Connect 3 pin connector to SBUS port on Rx module (box with two wires)
    1. (-) | Ground | Black
    2. (+) | Power  | Red
    3. (n) | Signal | White
2. Connect other end of connector to RCIN on CO+
    1. Keep in mind connection. Ground (GND) is on top
3. Connect RTK to CAN1 port. Should blink blue for Disarm
4. Run [Arm/Disarm Check](ArmDisarmCheck.md)
    1. Disarm Final

# BELOW REQUIRES BATTERY

## SiK Radio Setup

1. Connect Aircraft Radio to TELEM1 on Cube Orange+
2. Connect Home Radio to Computer running Mission Planner using USB Micro B cable
3. Attempt Connection remotely through mission planner (following Initial Connection Steps)
4. If successful, Mission Planner will provide the data stream and orientation output

## Motor Direction Test



6. [TEST LINK Text](README.md)



3. [TEST LINK Text](README.md)
