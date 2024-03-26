# Birdnet
Using Birdnet to detect birds songs using the RTSP audio provided by IP Camera  

### BirdnetPi on Proxmox
Start by creating an LXE in Proxmox using the following tutorial  
https://github.com/MatthewBCooke/BirdNET-Pi/blob/debian/setup/README.md  
Finish the setup using the following tutorial from Step 21  
https://github.com/mcguirepr89/BirdNET-Pi/wiki/Installation-Guide  

### RTSP Audio Stream
For adding a RTSP/ONVIF audio stream, coming from a IP camera for example, we have 2 options:  
**1:** Connect to the RTSP stream from the camera directly  
**2:** Use Go2RTC to connect camera's to your 'server' and distribute from there  
I would advise to use Go2RTC as a video/audio distributing platform, so there is only 1 active datastream from/to the IP camera itself (bandwith efficiensy and some IP camera's have issues maintaining more than 1 active RTSP stream)  


