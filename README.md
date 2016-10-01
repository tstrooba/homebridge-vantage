# VantagePlugin
VantageControls InFusion plugin for homebridge: https://github.com/nfarina/homebridge

# Installation
Install plugin with npm install -g homebridge-vantage
Add platform within config.json of you homebridge instance:

    {
        "platforms": [{
            "platform": "VantageControls",
            "ipaddress": "192.168.1,1"
            }], 
        "bridge": {
            "username": "CC:22:3D:E3:CE:31", 
            "name": "Vantage HomeBridge Adapter", 
            "pin": "342-52-220", 
            "port": 51826
        }, 
        "description": "My Fantastic Vantage System", 
        "accessories": []
    }

Restart homebridge
Enjoy!

# Supported Devices

Currently it should be possible to control all loads registered on you InFusion device, but I'm working on the detection of the difference with Relay, Dimmer and RGB Loads; I'm ready to support Thermostats and other devices but I prefer to keep the program stable before publish further functionalities. My test plan consists of:
- RGB Philips Hue lights and Osram Lightify (controlled by Vantage, my Hue Bridge is not compatible with HomeKit and I'm happy of this)
- LiFX (controlled by Vantage)
- Legrand/BTicino MyHome Relay and Dimmer
- Legrand/BTicino MyHome Thermostat
- Youus DMX Driver

Stay tuned!

# TODOS

- manage multiple feedbacks coming from the InFusion Controller when multiple values are sent from HomeKit
- test with standard Relay/Dimmer devices (...ehm...)

# Disclaimer

I'm furnishing this software "as is". I do not provide any warranty of the item whatsoever, whether express, implied, or statutory, including, but not limited to, any warranty of merchantability or fitness for a particular purpose or any warranty that the contents of the item will be error-free.
The development of this module is not supported by Vantage Controls or Apple. These vendors and me are not responsible for direct, indirect, incidental or consequential damages resulting from any defect, error or failure to perform.  