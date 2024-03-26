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

### Connect to MQTT and Home Assistant
Guide used for connecting and sending the BirdnetPi results to MQTT and Home Assistant (I Modified the script based on my needs, see birdnet_to_mqtt.py)  
https://gist.github.com/deepcoder/c309087c456fc733435b47d83f4113ff

### Screenshots and config
![image](https://github.com/kippesikgithub/birdnet_install/assets/100353268/e8023f62-c776-4ba3-b326-98e87196616c)  
Default username/password for config/tools  

![image](https://github.com/kippesikgithub/birdnet_install/assets/100353268/b789952a-ce69-4dc9-b8b4-788123b3b837)  
Top 10 Birds example (BirdNetPi frontpage)  

![image](https://github.com/kippesikgithub/birdnet_install/assets/100353268/7c037dc6-2a61-482c-bd9d-b0d7dd4a5249)  
Species stats example  

![image](https://github.com/kippesikgithub/birdnet_install/assets/100353268/edb9ab05-164f-41f6-a448-f537a66f4179)  
RTSP config

![image](https://github.com/kippesikgithub/birdnet_install/assets/100353268/b0766ce2-5d19-4c4b-8159-dc008423ca80)  
![image](https://github.com/kippesikgithub/birdnet_install/assets/100353268/eeb94ba5-0567-4098-8447-3c32ccc9151e)  
Tensorflow model config  




