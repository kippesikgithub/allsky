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

#### Prepare the RPI
I use this method because my ZWO ASI120MC is not really well supported by linux. But running it on a RPI3B using astroberry and ekos to expose an INDI server, works very well. This solution can also be used with other ZWO cams, and is basically using the RPI to get your ZWO cam on your wifi network and controll them.  
install Astroberry on your RPI  
start KStars  
start EKOS  
in EKOS configure your camera  
get the IP address and port of the INDI server on the RPI (in EKOS)  


#### Install Indi-Allsky
Using Debian as Linux base before installing indi-allsky.  
Install indi-allsky in 'INDI' mode, so it makes it accept INDI cameras from remote RPI.  
![image](https://github.com/user-attachments/assets/0cf1252d-3787-4bb1-973d-c98bef9f21a0)  

#### Config Indi-Allsky
For configuring indi-allsky with a ZWO camera that is running on a remote RPI we need to add the INDI details from the RPI.  
Fill in the camera/stream details in the given area for the INDI server. the INDI server is running on a rpi 3b in the box.  

My setups are only capturing during the night, so switched off day-time capture.  
![image](https://github.com/user-attachments/assets/d0ff9402-5dc9-4155-8fae-34e77235364f)  


