# Crestron-Sensibo-Pure-Integration

This module provides control of a Sensbo Pure air purifier from a Crestron
3-Series or 4-Series Processor.  

The first step in using this module is to obtain an API Key.  To accomplish 
this you will need to use your username/password and login to the Sensibo 
web site.  There is a login link in the menu at the bottom of the main 
page of the web site.  You will then be presented with a screen that shows 
you your Sensibo devices.  In the upper left hand corner of the screen is 
a menu icon and selecting it will present you with an option to create an 
API Key.

Next you will need to obtain the ID of your Sensibo Pure.  In the lower right
corner of the square that represents you Sensibo Pure when you are logged in on
the Sensibo web site is a 3 dot menu icon.  Pressing this displays a drop down
menu.  Press the "Advanced" option on the menu and then choose "Advanced Info".
The UID is the device ID of your Sensibo Pure.

Copy the API Key and the UID into the API_Key and Device_ID paramters of this
module. 

Inputs
Initialize       - Must be pulsed to initilize communications
Refresh          - Will referesh the status of feedback signals.
                   Shouldn't be needed unless someone controls
                   the Sensibo Pure using the buttons on the
                   device or the app.
Purifier_On/Off  - Pulse to turn purifer on or off
Light_On/Dim/Off - Pulse to control the Purifier's light
PureBoost_On/Off - Pulse to turn Pure Boost on/off
Fan_Low/High     - Pulse to control the fan speed

Outputs
Purifier_*_FB    - Power status of purifier
Light_*_FB       - Status of the purifier's light
PureBoost_*_FB   - On/Off status of Pure Boost Mode
Fan_*_FB         - Fan speed status
PM25             - 1 = Good Air Quality, 2 = Moderate Air 
                   Quality, and 3 = Unhealthy Air Quality

Parameters
Device_ID        - UID of device to be controlled obtained
                   from the Sensibo web site
API_Key          - API Key from Sensibo web site
Debug_Msg_Output - Where to send debug messages
                   0=None, 1=Console, 2=Error Log, 3=Both 
