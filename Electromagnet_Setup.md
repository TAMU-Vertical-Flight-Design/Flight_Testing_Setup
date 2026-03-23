# Electromagnet Setup

For the ARDUPILOT and Transmitter set up, they should already be configured, but if not the steps for setup are below.

**ARDUPILOT SETUP**
1. Set Servo13_FUNCTION to “-1”       (Turns off conflicting servo functionality)
2. Set FLTMODE_CH to “7”              (Changes conflicting flight mode functionality to a different channel)
3. Set RELAY1_FUNCTION to “1”         (Turns on Relay functionality)
4. Write Parameters                   (Must do this before next step)
5. Set RELAY1_PIN to “54” (Aux 5)     (Assigns Relay functionality to Aux 5 port)
6. Write Parameters
7. Set RC5_OPTION to "28" (Relay1 on/off)
8. Navigate to the “Data” tab for use

**TARANIS Transmitter setup**
1. Press the MENU button
2. Page 1/13 - MODEL SELECTION, should open, navigate with the roller to the correct profile, press and hold down the roller, then click "select model" with the roller.
    - If using Mini-Rev use number 27 DBVFTESTmini
    - If using Rev3 use number 26 DBVFTEST
3. Navagate to page 4/13 - INPUTS, scroll through and see if any are named EMAG or something similar. Hold click and select Edit.
   - If there is none
     - find and empty input, the name should be a number with no assigned input to the right of it
     - click it with the roller
     - On input name give it a name like EMAG uing the roller, you can press the EXIT button when you are done entering the letters
   - Scroll to "Source" and click it. when you press different switches and buttons on the controller you should see different things appear corrosponding to what you touched. Flip the big switch where the right trigger would be positioned on a traditional game controller. It should be the one that springs back down after you flip it. You should see SH appear. Press Exit when done
   - Scroll to "Weight" and set it to -100, this makes the low position on by default and flipping it up turn the Emag off
   - Press the Exit button to get back to the Inputs page, you should now see an input called Emag with -100 and "SH" to its right
4. Navigate one page over to 5/13 - MIXES
   - Scroll down to CH5 and repeat the same proccess you did in step 3 in this channel. The previous step told the transmitter to look that the SH switch as an input, this step tells it to brodcast that switches inputs on channel 5.
  
You Can test if this worked by taking a multi meter and putting the ground cable to the top pin, and the positive cable to the bottom pin of AUX 5


**Description of hardware**
- MOSFET - Large board with 3 large terminals (VIN, GND, VOUT) and a 3pin signal cable (Black, Red, Green) on the opposite end.
- BEC - Small board connected to the VIN (red) and GND (white) of the MOSFET, and two output jumper connections (out red, G white)

**For REV MINI**
1. Connect the 2 connecter pins from BEC to AUX 1, make sure ground (white) is on the top and the positive (red) is in the middle
2. Connect the 3-pin signal wire from MOSFET to AUX 5
3. (READ ALL) Connect the battery, everything is active once plugged in, so as soon as you touch one XT60 connector to the other, be vigilant for weird sounds, smoke, or components over heating. If anything out of place happens immediately unplug the battery so long as it is safe to. The only exception is small temporary pops, small arcs might happen right when plugging in, but it should be small any very temporary.
4. Check if the BEC light turns on, solid red = good
5. The Emag should now be on as the Emag is on by default, It should turn off when you flip the switch up on the transmitter 

**For REV 3**
1. Ensure the BEC is not connected to the MOSFET, it will not be used
2. Connect the 3-pin signal wire from MOSFET to AUX 5
3. (READ ALL) Connect the battery, everything is active once plugged in, so as soon as you touch one XT60 connector to the other, be vigilant for weird sounds, smoke, or components over 3. heating. If anything out of place happens immediately unplug the battery so long as it is safe to. The only exception is small temporary pops, small arcs might happen right when plugging in, but it should be small any very temporary.
5. Check if the BEC light turns on, solid red = good
6. The Emag should now be on as the Emag is on by default, It should turn off when you flip the right most bottom most switch up (it springs back down after you flip it up to keep the Emag 
