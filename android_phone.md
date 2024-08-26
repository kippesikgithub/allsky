# Manual using a Android Phone with Indi-Allsky
I mostly use this setup on Holiday or when I know there's something to happen tonight. Just having this as an extra solution is great.  
When you have an Old Android phone laying around, this is an easy setup.  

### Requirements
Android phone (can be older model)  
Android app IP webcam  
powersupply or powerbank  
wifi connection  
Proxmox Ubuntu 22.04 LXC  
Indi-Allsky installed in the Proxmox Ubuntu LXE  
Indi-Allsky mode: pycurl  

#### Prepare Android Phone
1) install android app IP webcam from google app store
2) open the app, select the right camera and preferred resolution.
3) push the hamburger menu, and press 'start server'
4) from now on you can reach the web interface on http://ipphone:8080
5) optionally give your phone a static IP om your network
6) continue in the webinterface
7) click the 'overlay' to display time and date
8) setup the focus
9) setup the iso and exposure (differs per phone whats the max exposure. for my google pixel 4xl it maxes out at 10s)

#### Install Indi-Allsky
Using Debian as Linux base before installing indi-allsky.  
Install indi-allsky in 'pycurl' mode, so it makes it accept jpeg streams from your IP camera.  

#### Config Indi-Allsky
Fill in the camera/stream details in the given area for PyCurl camera.  
The details are shown in the Android IP webcam app, and differ from what you see in the screenshot here.  
![image](https://github.com/user-attachments/assets/fdc3e001-cd6f-4b34-aec1-aa6f18026290)  
