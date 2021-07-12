<h1>Adding Sonoff To Home Assistant</h1>

Tutorial on how to add sonoff switches to home assistant

<h1> Prerequisite </h1>
* [Ewelink App](https://play.google.com/store/apps/details?id=com.coolkit&hl=en&gl=US) and account
* [Sonoff S26 - UK Type WiFi Smart Power Socket Adapter](https://my.cytron.io/p-sonoff-s26-uk-type-wifi-smart-power-socket-adapter)
* Home Assistant with HACS installed
* Raspberry Pi 4 or equilvalent


<h1>Tutorial Overview</h1>

[Download Ewelink App](https://play.google.com/store/apps/details?id=com.coolkit&hl=en&gl=US) and register an account

Pair the devices to the app

Click on HACS > Integration > Explore & Add Repositories > Sonoff LAN > Install this repositories in HACS
Sonoff folder containing custom component will be added into home-assistant/custom_components/

[Credits go to AlexxIT](https://github.com/AlexxIT/SonoffLAN)

SSH into Pi

Edit the configuration.yaml file

sudo nano /config/home-assistant/configuration.yaml 

![image](https://user-images.githubusercontent.com/87014174/125241866-9566d300-e31e-11eb-8216-6e866e41be13.png)

Add the following:
sonoff:                                                                                                                   
   username: your-EWELINK-login-Email                                                                                         
   password: your-password                                                                                                    
   mode: local                                                                                                             
   reload: always 
Be mindful of the tab arrangements or there will be errors when you restart home assistant

Restart home assistant

You should be able to see a list of sonoff paired devices listed in home assistant developer Tools
![image](https://user-images.githubusercontent.com/87014174/125242711-a237f680-e31f-11eb-9eb8-72b56b01deff.png)




