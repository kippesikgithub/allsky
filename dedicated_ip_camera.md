# Manual using a dedicated (POE) Ip camera with Indi-Allsky

### Requirements
Ip Camera providing a JPEG or MJPEG stream (if your cam only provides onvif/rtsp or only a low quality snaphot, create one yourself using Go2RTC)  
Proxmox Ubuntu 22.04 LXC  
Indi-Allsky installed in the Proxmox Ubuntu LXE  
Indi-Allsky mode: pycurl  

#### Prepare IP Camera
Since using an IP camera, indi-allsky won't be able to configure the camera. You have to configure the camera yourself in the webinterface provided by the camera. 
Try to find some settings which will show you most stars in the night, changing the gain/exposure/other settings. More clear skies make it easier to configure the settings.  

#### Install Indi-Allsky
Using Debian as Linux base before installing indi-allsky.  
Install indi-allsky in 'pycurl' mode, so it makes it accept jpeg streams from your IP camera.  
![image](https://github.com/user-attachments/assets/df21f0ec-df88-4475-a254-1e6629ee61d8)  


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
