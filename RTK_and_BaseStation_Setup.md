This file details how to setup the Here4 RTK and Base Station for GPS corrections on mission planner. Note, this tutorial does not include setup of the telemetry radio system for communication with the RTK. The base station communicates with the CubeOrange directly via USB in this tutorial. 

Neccessary Hardware: Personal Laptop with Mission Planner installed, CubeOrange, Here4 RTK, Here4 Base Station. 

Step 1. Plug Blue/Green wire from the RTK connection into "COM1" on the CubeOrange, the Here4 RTK should begin blinking indicating that it is searching.

Step 2. Plug the Base Station into your computer via USB.

Step 3. Plug CubeOrange into your computer with a Micro-b to USB cable. 

Step 4. Open mission planner and click "Connect" in the top right corner to connect to the CubeOrange. 

Step 5. Click "Config" then "Full Parameter List".

Step 6. Set "Can_P1_Driver" value to 1. 

Step 7. Set "GPS_Type" to 9. 

Step 8. Click "Write Params" to save changes to the full parameter list. 

Step 9. Click "Setup", then "Optional Hardware", then "DroneCAN/UAVCAN"

Step 10. Click the drop down and select "MAVLinkCAN1" then hit connect. You should see the cubepilot.here4, this is a confirmation to make sure the RTK is being read. 

<img width="1919" height="1218" alt="image" src="https://github.com/user-attachments/assets/f32abf66-1dd8-4502-8f46-58e517307bb8" />

Step 11. Click "GPS/RTK inject".

Step 12. Select "COM10" on the dropdown in the right hand corner. Note this isn't necessarily always COM10, but the selected port needs to be the input port of the base station. 

Step 13. Check the "Automatically Configure Reciever" box. A new menu should show up with the capability to configure the base station, select the "Ublox M8P / F9P" dropdown.

Step 11. Type desired GPS position accuracy into the "Survey in acc" box, then click "Restart" to configure the base station. Note expect somewhere between 5 - 10 minutes for the configuration of the base station. 

<img width="375" height="32" alt="image" src="https://github.com/user-attachments/assets/eaa8317c-fa81-4571-a86d-384d4e0e12b2" />

Once the base station is done configuring the output should look like this: 

<img width="1919" height="1100" alt="image" src="https://github.com/user-attachments/assets/7dbb46b5-bfd6-4c58-a04b-4137e6f78ec9" />

In order to check the output of the RTK, you can hit cntrl+F, then "Mavlink inspector". 

<img width="723" height="552" alt="image" src="https://github.com/user-attachments/assets/6d2e0549-92dd-47e1-8bdf-4b964366fd19" />

