# Allsky Setups
Some documentation about my indi-allsky setups for nightlapses, stargazing, northern light, runnig on Proxmox LXE. Using old Android phones and IP camera's to capture the nightsky and all thats happening above us when we are asleep.

#### Why?
The night-sky is amazing isn't it? Even here in the Netherlands with a lot of light pollution, there is a lot to see at night in the sky, but we are asleep by then. As a Techie, Data and Automation guy I found some interesting posts on the www of people using specific made Astro camera's combined with Indi-Allsky (https://github.com/aaronwmorris/indi-allsky) software, running on a RPI. Creating Timelapses, Keograms, Panorama's, Startrails and much more, fully automated every night. Since I already own 2 proxmox servers, and have a lot experience using IP camera's, a new idea was born. What if i could use Old phones and IP camera's to do the same, comined with Indi-Allsky.  

Some more details on the proces I had to go through, for creating a 1-2 minute timelapse of the night sky: Manually setting up an Old android phone in our garden, go through all the settings manually on the phone in the 'Deepsky' app (https://www.deepskycamera.de/), and offcourse connect the phone to a large powerbank, transferring (tons of) pictures manually and creating night-timelapses manually the morning after, thansferring back the video to phone and server manually. As you can imagine, this costed a lot of time and effort, resulting in just a short video.  

Having a lot of luck, the guy creating the Indi-allsky (https://github.com/aaronwmorris/indi-allsky) software, created a way to connect to the JPEG stream of a network/IP camera. After some searching around, finding out there are not that many people using this kind of setup, I found a way to make it all work. And the best part, I finished finetuning the setup, just a couple of nights before the Northern lights storm (10-05-2024), and captured great content! Because there is so little information about this kind of setup, I created this documentation, as a guide.  


## My 3 setups

#### Permanent Setup
POE IP camera mounted outside in our backyard, pointed upwards (offcourse), with a 180 degree lens.  
![image](https://github.com/user-attachments/assets/3011530c-0e2e-49f3-ae77-6972dfaf5091)

**Hardware**  
Camera: REVODATA 5MP Mini Fisheye POE IP Camera, lens 1.7mm 180 degree, waterproof  
Software: Indy Allsky in a Ubuntu 22.04 Proxmox LXC  
Streaming App: Go2RTC (proxmox lxe or Home assistant addon)  

#### ZWO Setup
ZWO ASI120MC, in a lunchbox with a 160 degree lens  
Raspberry Pi 3b as INDI server  
esp32 with dallas and dht11 temp/humidity sensors  
![image](https://github.com/user-attachments/assets/275de39e-613f-4cf0-a3fc-bca714b5cbd0)

**Hardware**  
Camera: ZWO ASI120MC (ubs2 old version), lens 160 degree    
Waterproofing: Lunch-Box (Hema), Dome from old Samsung IP camera  
Software: Indy Allsky in a Ubuntu 22.04 Proxmox LXC  
Power: 6mtr cable, 12v 2A Adapter, 12->5V converter, usb-c connector  
Esp32 super mini board  
Dallas temp sensor  
DHT11 temp/humidity sensor  
5v Relais for dewheater in dome  
12 x 30ohm resistors as dew heater  
RPI 3b running astroberry serving the ZWO camera to Proxmox LXC over INDI protocol  

#### Portable Setup
Google Pixel 4XL Android phone  
modified, removed battery, powered by powerbank  
![image](https://github.com/user-attachments/assets/4cf73977-2484-4b5a-916b-df52a283436e)

**Hardware**  
Camera: Google Pixel 4XL Android Phone, lens 240 degree  
Android App: IP Webcam (transform your android phone in a IP camera)  
Software: Indy Allsky in a Ubuntu 22.04 Proxmox LXC  
Direct usb power or Powerbank 20000mah  
No waterproofing  
  

## Howto's

**Proxmox LXC Setup**  
https://github.com/kippesikgithub/allsky/blob/main/proxmox_lxc_setup.md  

**Permanent Setup using a dedicated (POE) IP Camera**  
https://github.com/kippesikgithub/allsky/blob/main/dedicated_ip_camera.md  

**ZWO Setup using a ZWOASI120MC Camera**
https://github.com/kippesikgithub/allsky/blob/main/zwo_asi120mc.md  

**Portable Setup using a Android Phone**  
https://github.com/kippesikgithub/allsky/blob/main/android_phone.md  

## Result Examples
#### Google Pixel 4XL Nothern Lights storm (10-05-2024)
Setup: Portable Setup  
![image](https://github.com/kippesikgithub/allsky/assets/100353268/19a2e81d-b3ba-4a7b-8c31-dd776e4d48ac)  
youtube link: https://www.youtube.com/watch?v=eyGsOYiEsdU  

#### ZWOASI120MC Clear Night (11-08-2024)
Setup: ZWO Setup  
![image](https://github.com/user-attachments/assets/cd24eb3e-8e6b-45d1-83f0-d1746737f859)  

#### ZWOASI120MC Cloudy Night (25-08-2024)
Setup: ZWO Setup  
![image](https://github.com/user-attachments/assets/6c848566-66f2-40b0-aa98-54e42f440991)  

#### Poe IP Camera Clear Night (11-08-2024)
Setup: Permanent Setup  
![image](https://github.com/user-attachments/assets/21c08c43-aa07-46d8-b1a4-7137a249f641)  

#### Poe IP Camera Cloudy Night (24-08-2024)
Setup: Permanent Setup  
![image](https://github.com/user-attachments/assets/c42f3b9d-35e4-4c88-bc31-b5ddf5631e3b)  

####  Star Trail Comparison (11-08-2024)
Setup: Poe IP Camera vs ZWOASI120MC  
![image](https://github.com/user-attachments/assets/22e4ed0d-395c-4bb7-b52c-ea3bfc8e46be)  




