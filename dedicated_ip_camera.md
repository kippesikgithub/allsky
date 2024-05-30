# Manual using a dedicated (POE) Ip camera with Indi-Allsky

### Requirements
Ip Camera providing a JPEG or MJPEG stream (if your cam only provides onvif/rtsp or only a low quality snaphot, create one yourself using Go2RTC)  
Proxmox Ubuntu 22.04 LXC  
Indi-Allsky installed in the Proxmox Ubuntu LXE  
Indi-Allsky mode: pycurl  

#### Prepare IP Camera

#### Install Indi-Allsky

#### Config Indi-Allsky

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
