# Home-Assistant-Broadlink-MP1-Custom-Component (Above HA Version 0.92.1)
There is a sync delay in official component for Broadlink MP1 of HA. This code resolved the issue! (Tested in HA version 0.92.1)


If you are using a Broadlink MP1(or MP1s), you have seen the sync delay when you turn on/off some slot with short interval.
This code fixed the issue.


To use this, you have create a custom_components/broadlink_mp1 directory in your config directory and copy & paste 5 files.



ex>

/home/homeassistant/.homeassistant/custom_components/broadlink_mp1/__init__.py

/home/homeassistant/.homeassistant/custom_components/broadlink_mp1/const.py

/home/homeassistant/.homeassistant/custom_components/broadlink_mp1/manifest.json

/home/homeassistant/.homeassistant/custom_components/broadlink_mp1/services.yaml

/home/homeassistant/.homeassistant/custom_components/broadlink_mp1/switch.py



In the configuration.yaml (or switch.yaml), you have to add the 4 switches like the below.


switch:

#Broadlink Livingroom MP1

  - platform: broadlink_mp1
  
    host: 192.168.0.9
    
    mac: 'B4:43:0D:AA:AA:AA'
    
    type: mp11
    
    friendly_name: 'Livingroom MP1 SW 1'
    
    

  - platform: broadlink_mp1
  
    host: 192.168.0.9
    
    mac: 'B4:43:0D:AA:AA:AA'
    
    type: mp12
    
    friendly_name: 'Livingroom MP1 SW 2'
    
    
    
  - platform: broadlink_mp1
  
    host: 192.168.0.9
    
    mac: 'B4:43:0D:AA:AA:AA'
    
    type: mp13
    
    friendly_name: 'Livingroom MP1 SW 3'
    
    
    
  - platform: broadlink_mp1
  
    host: 192.168.0.9
    
    mac: 'B4:43:0D:AA:AA:AA'
    
    type: mp14
    
    friendly_name: 'Livingroom MP1 SW 4'
    


The mac is the MP1's mac address and the host is a IP address of the MP1.


If you set up, you can get the 4 switches and you can expose them in your frontend.

switch.livingroom_mp1_sw_1

switch.livingroom_mp1_sw_2

switch.livingroom_mp1_sw_3

switch.livingroom_mp1_sw_4
