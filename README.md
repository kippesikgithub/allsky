# Allsky Setups
Some documentation about my indi-allsky setups for nightlapses, stargazing, northern light, runnig on Proxmox LXE. Using old Android phones and IP camera's to capture the nightsky and all thats happening above us when we are asleep.

#### Why?
The night-sky is amazing isn't it? Even here in the Netherlands with a lot of light pollution, there is a lot to see at night in the sky, but we are asleep by then. As a Techie, Data and Automation guy I found some interesting posts on the www of people using specific made Astro camera's combined with Indi-Allsky (https://github.com/aaronwmorris/indi-allsky) software, running on a RPI. Creating Timelapses, Keograms, Panorama's, Startrails and much more, fully automated every night. Since I already own 2 proxmox servers, and have a lot experience using IP camera's, a new idea was born. What if i could use Old phones and IP camera's to do the same, comined with Indi-Allsky.  

Some more details on the proces I had to go through, for creating a 1-2 minute timelapse of the night sky: Manually setting up an Old android phone in our garden, go through all the settings manually on the phone in the 'Deepsky' app (https://www.deepskycamera.de/), and offcourse connect the phone to a large powerbank, transferring (tons of) pictures manually and creating night-timelapses manually the morning after, thansferring back the video to phone and server manually. As you can imagine, this costed a lot of time and effort, resulting in just a short video.  

Having a lot of luck, the guy creating the All-sky (https://github.com/aaronwmorris/indi-allsky) software, created a way to connect to the JPEG stream of a network/IP camera. After some searching around, finding out there are not that many people using this kind of setup, I found a way to make it all work. And the best part, I finished finetuning the setup, just a couple of nights before the Northern lights storm (10-05-2024), and captured great content! Because there is so little information about this kind of setup, I created this documentation, as a guide.  

![image](https://github.com/kippesikgithub/allsky/assets/100353268/19a2e81d-b3ba-4a7b-8c31-dd776e4d48ac)  
youtube link: https://www.youtube.com/watch?v=eyGsOYiEsdU  
The result of a setup using a Google Pixel 4XL as camera (ISO 800, 10sec exposure) combined with Indi-Allsky

#### My 2 setups

##### Permanent Setup
POE IP camera mounted outside in our backyard, pointed upwards (offcourse), with a 180 degree lens.

###### Hardware
camera: https://www.amazon.nl/REVODATA-ingebouwde-microfoon-Beveiligings-Bewegingsdetectie/dp/B0C7Z9JJFH/ref=sr_1_46?dib=eyJ2IjoiMSJ9._396fqAZ8VULtihukLmlPksaWepg3sYZMxFYEZGdzu8ixolkg0gGuLhX2rpfc5BB-g11Z3ImE_-yBsaCrwzEWmNFFHyQzrtYIq7pENhk1YrL0-Ms9rOjxWY23yDLb78FiDyuR6KFWlfzZtG9RKXNOn024FMX1hOUBMuvcoK4CDslW1kpV_GXtJc60EGv8uIZSv-z5G044rNMHPZ4SVxjobd5OeXKlLdCnzPsz1bWItsDxc0oATEwV_lp8SzsMALjYx2iIAe3_mM3eWgHpYLSqNKPxpH9y2fvQ1ATri9ykG0.3pxTRkgHoROwZ3Tpmb8yPq1h4-Qs7sIzYkiCF9daplo&dib_tag=se&keywords=IMX291%2BIP%2Bcamera&qid=1715715439&sr=8-46&th=1
##### Portable Setup
