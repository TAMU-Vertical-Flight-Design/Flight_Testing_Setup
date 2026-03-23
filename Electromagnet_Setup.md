# Electromagnet Checklist

ARDUPILOT SETUP
1. Set Servo13_FUNCTION to “-1”       (Turns off conflicting servo functionality)
2. Set FLTMODE_CH to “0”              (Turns off conflicting flight mode functionality)
3. Set RELAY1_FUNCTION to “1”         (Turns on Relay functionality)
4. Write Parameters                   (Must do this before next step)
5. Set RELAY1_PIN to “54” (Aux 5)     (Assigns Relay functionality to Aux 5 port)
6. Write Parameters
7. Navigate to the “Data” tab for use



Description of hardware
- MOSFET - Large board with 3 large terminals (VIN, GND, VOUT) and a 3pin signal cable (Black, Red, Green) on the opposite end.
- BEC - Small board connected to the VIN (red) and GND (white) of the MOSFET, and two output jumper connections (out red, G white)

For REV MINI
1. Connect the 2 connecter pins from BEC to AUX 1, make sure ground (white) is on the top and the positive (red) is in the middle
2. Connect the 3-pin signal wire from MOSFET to AUX 5
3. (READ ALL) Connect the battery, everything is active once plugged in, so as soon as you touch one XT60 connector to the other, be vigilant for weird sounds, smoke, or components over heating. If anything out of place happens immediately unplug the battery so long as it is safe to. The only exception is small temporary pops, small arcs might happen right when plugging in, but it should be small any very temporary.
4. Check if the BEC light turns on, solid red = good
5. The Emag should now be on as the Emag is on by default, It should turn off when you flip the switch up on the transmitter 

For REV 3
1. Ensure the BEC is not connected to the MOSFET, it will not be used
2. Connect the 3-pin signal wire from MOSFET to AUX 5
3. (READ ALL) Connect the battery, everything is active once plugged in, so as soon as you touch one XT60 connector to the other, be vigilant for weird sounds, smoke, or components over 3. heating. If anything out of place happens immediately unplug the battery so long as it is safe to. The only exception is small temporary pops, small arcs might happen right when plugging in, but it should be small any very temporary.
5. Check if the BEC light turns on, solid red = good
6. The Emag should now be on as the Emag is on by default, It should turn off when you flip the right most bottom most switch up (it springs back down after you flip it up to keep the Emag 
