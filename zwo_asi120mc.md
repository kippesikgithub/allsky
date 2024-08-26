# Manual using a ZWO ASI120MC with Indi-Allsky

![image](https://github.com/user-attachments/assets/1243b334-a4f5-4eff-855d-119a351ff775)  

### Requirements
Camera: A ZWO or other astro camera  
RPI 3b running astroberry serving the ZWO camera to Proxmox LXC over INDI protocol  
Proxmox Ubuntu 22.04 LXC  
Indi-Allsky installed in the Proxmox Ubuntu LXE  
Indi-Allsky mode: INDI  

#### Prepare IP Camera
Waterproofing: Lunch-Box (Hema), Housing and Dome from old Samsung IP camera  
Power: 6mtr cable, 12v 2A Adapter, 2x 12->5V converter  
Esp32 super mini board  
Dallas temp sensor  
DHT11 temp/humidity sensor  
5v Relais for dewheater in dome  
12 x 30ohm resistors as dew heater  

#### Install Indi-Allsky
Using Debian as Linux base before installing indi-allsky.  
Install indi-allsky in 'INDI' mode, so it makes it accept INDI cameras from remote RPI.  
![image](https://github.com/user-attachments/assets/0cf1252d-3787-4bb1-973d-c98bef9f21a0)  

#### Config Indi-Allsky
For configuring indi-allsky with an IP camera, we have to accept that the exposure and other settings are controlled by the camera itself. Using a JPEG (image driven) stream from the camera is the only way. 
If the camera doesn't provide one, see my solution using Go2RTC, and create your own.  

Fill in the camera/stream details in the given area for PyCurl camera.  
![image](https://github.com/user-attachments/assets/22c8e9e4-dbb0-43a0-b87a-4fc389359f84)  

My setups are only capturing during the night, so switched off day-time capture.  
![image](https://github.com/user-attachments/assets/d0ff9402-5dc9-4155-8fae-34e77235364f)  


#### Go2RTC as streaming
When your camera doesnt provide a JPEG or MPJEG stream, but does have onvif/rtsp  
1) Create a proxmox Go2RTC LXC from the proxmox helper scripts (https://helper-scripts.com/)
2) Configure Go2RTC to connect to your Ip camera by rtsp/onvif url (use windows tool Onvif device explorer to find the stream url, Optionally in VLC test your stream by opening a network stream, and copy-paste your rtsp url)
3) Save and restart Go2RTC
4) Click on the 'links' next to the camera you added
5) Search for the 'MJPEG source' topic
6) copy the url from the 'frame.jpeg'
7) use the copied link in Indi-Allsky as the source for your Indi-Allsky 'pyCurl Camera URL'  
![image](https://github.com/kippesikgithub/allsky/assets/100353268/2d737e3b-a8fe-4b8e-bee8-b3598f55387f)
