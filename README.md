# NSPanel-shaf
NSPanel-shaf is based on marcfagers original work and MarkWattTech update.

Thank you to @MarkWattTech for putting a Tutorial togther on how to flash the the Sonoff NSPanel (https://youtu.be/p-AK4o5jOSI).  I have taken what he has put togther and simplified the code for easier editing.   Addtioanlly, I also have created a new HMI to add addtioanl items to the the Main Page.   

We will work on getting a video upload to our youtube Channel https://www.youtube.com/SmartHomeAF, in the meantime use @MarkWattTech channel to get Started and use my nspanel.yaml and hmi.tft files.


## Credits

marcfagers - https://github.com/marcfager/nspanel-mf

MarkWattTech https://github.com/MarkWattTech/MWT-NSPanel

## Usage
The weather entities, media entities, lights etc. are selected in the ESPHome config (nspanel.yaml). You can navigate between screens by using a swipe gesture on the screen (left or right). The code is prepared for swipe up and down as well. The media player is on the left side, and the lights on the right side.

In the example config a big part of the config is done in the nspanel.yaml file.   See Configuration below on what shoudl be changed.

Any information and/or code found here is used on your own risk.

## Installation
1. Install and configure ESPHome.   Use the nspanel.yaml "as is" for instalation.
2. Prepare the NSPanel for flashing (see MarkWattTech Video https://youtu.be/p-AK4o5jOSI).
3. Download the ESPHome sketch and adjust to your needs. Flash it to the NSPanel. Pay special attention to the _tft_url_ parameter and ensure it is accessible by the NSPanel.
4. Download the HMI.tft file and save it to the _tft_url_ location.
5. Add the unit to Home Assistant through the ESPHome integration.
6. Run the _esphome.nspanel_upload_tft_ service from Home Assistant. This will download the HMI to the NSPanel. Please note that this will block the ESPHome connection during the update. Follow the progress on the HMI screen. When the HMI is installed, reboot the unit.
7. Use steps in the Configuration Section below to customize what is being displayed in the LCD

## Configuration
- In the ESPHome Addon Edit the NSPanel Device 
<img width="611" alt="image" src="https://user-images.githubusercontent.com/105226208/167456356-8dd6e3a5-9308-4008-a3f3-abe982b1d067.png">
- Modify the highlighted section with your entities. 
<img width="611" alt="image" src="https://user-images.githubusercontent.com/105226208/167457166-71f64c7e-3169-46bc-9130-f4d67d76fa06.png">

- Validate the Config
- Install Config Wirelessly

- 
