# Manual using a Android Phone with Indi-Allsky

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

#### Config Indi-Allsky
