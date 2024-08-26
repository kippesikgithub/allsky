# Manual using a ZWO ASI120MC with Indi-Allsky

![image](https://github.com/user-attachments/assets/1243b334-a4f5-4eff-855d-119a351ff775)  

### Requirements
Camera: A ZWO or other astro camera  
RPI 3b running astroberry serving the ZWO camera to Proxmox LXC over INDI protocol  
Proxmox Ubuntu 22.04 LXC  
Indi-Allsky installed in the Proxmox Ubuntu LXE  
Indi-Allsky mode: INDI  

#### Prepare the ESP32 (optional)
Since I use Home Assistant (with EspHome) very heavily, I created my own sensors for in the Box and Dome.  
Esp32 with EspHome config for 1 Temperature sensor in the box, 1 Temperature and Humidity sensor in the Dome, Relais with Dewheater in the Dome.  
Some Node Red automation flows controlling the dewheater, using the dewpoint.   
Esp32 super mini board  
Dallas temp sensor  
DHT11 temp/humidity sensor  
5v Relais for dewheater in dome  
12 x 30ohm resistors as dew heater  

#### Prepare IP Camera and Housing
Waterproofing: Lunch-Box (Hema), Housing and Dome from old Samsung IP camera  
Power: Laptop Adapter 18.5v 3.82A, 6mtr cable  
Buck convertors 2x input:8-24 -> output:5V 5A converter  

#### Prepare the RPI
I use this method because my ZWO ASI120MC is not really well supported by linux. 
But running it on a RPI3B using astroberry and ekos to expose an INDI server, works very well.  
This solution can also be used with other ZWO cams, and is basically using the RPI to get your ZWO cam on your wifi network and controll them.  

1) Install Astroberry on your RPI  
2) Start KStars  
3) Start EKOS  
4) In EKOS configure your camera
5) Click the 'Play' button in EKOS
6) Click 'Connect' in EKOS  
7) get the IP address and port of the INDI server on the RPI (in EKOS)  
Now you can reach your camera over IP and Port in your network, and controll them like they are locally connected  

#### Install Indi-Allsky
Using Debian as Linux base before installing indi-allsky.  
Install indi-allsky in 'INDI' mode, so it makes it accept INDI cameras from remote RPI.  

#### Config Indi-Allsky
For configuring indi-allsky with a ZWO camera that is running on a remote RPI we need to add the INDI details from the RPI.  
Fill in the camera/stream details in the given area for the INDI server. The INDI server is running on a rpi 3b in the box, so you fill in the IP and Port of the RPI.  
![image](https://github.com/user-attachments/assets/73af61cc-7f57-4156-817e-2823b468934d)

My setups are only capturing during the night, so switched off day-time capture.  
![image](https://github.com/user-attachments/assets/d0ff9402-5dc9-4155-8fae-34e77235364f)  


