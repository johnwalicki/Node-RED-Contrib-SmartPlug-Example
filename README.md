## EdiMax SmartPlug / TI SensorTag 3200 WiFi Example
---
This example uses a 
[WiFi connected TI SensorTag 3200](https://developer.ibm.com/recipes/tutorials/texas-instruments-cc3200-simplelink-wifi-sensortag/)
to control an 
[EdiMax SmartPlug](http://www.edimax.com/edimax/merchandise/merchandise_detail/data/edimax/global/home_automation_smart_plug/sp-2101w/)
that turns on and off a space heater in my home office. I only want the heater to be on when
the lights are on and the temperature is low.  If I'm not working and the lights are off,
I don't need to heat the basement room that I use as my home office.

I created some Node-RED [flows](flow.json) that query the temperature and luminosity from the TI SensorTag once a minute.
The flow uses the [node-red-contrib-smartplug nodes](https://flows.nodered.org/node/node-red-contrib-smartplug) to turn on/off the SmartPlug.

I also created a simple Node-RED Dashboard to display power consumption and adjust the "thermostat".
![Node-RED Dashboard SmartPlug SensorTag](SmartPlug-Dashboard.png?raw=true "Node-RED Dashboard SmartPlug SensorTag")

Here are the two Node-RED flows:
![Node-RED SmartPlug flow](SmartPlug-Dashboard-flow.png?raw=true "Node-RED SmartPlug flow")
![Node-RED SensorTag WiFi](SensorTagWiFi-SmartPlug-flow.png?raw=true "Node-RED SensorTag SmartPlug flow")

