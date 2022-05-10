# NSPanel-shaf
NSPanel-shaf is based on marcfagers original work and MarkWattTech update.

Thank you to @MarkWattTech for putting a Tutorial togther on how to flash the the Sonoff NSPanel (https://youtu.be/p-AK4o5jOSI).  I have taken what he has put togther and simplified the code for easier editing.   Addtioanlly, I also have created a new HMI to add additional items to the the Main Page.   

We will work on getting a video uploaded to our youtube Channel https://www.youtube.com/SmartHomeAF, but in the meantime use @MarkWattTech channel to get Started and use my nspanel.yaml and hmi.tft files instead.


## Credits

marcfagers - https://github.com/marcfager/nspanel-mf

MarkWattTech https://github.com/MarkWattTech/MWT-NSPanel

## Usage
The weather entities, media entities, lights etc. are selected in the ESPHome config (nspanel.yaml). You can navigate between screens by using a swipe gesture on the screen (left or right). The code is prepared for swipe up and down as well. The media player is on the left side, and the lights on the right side.

In the example config a big part of the config is done in the nspanel.yaml file.   See Configuration below on what shoudl be changed.

Any information and/or code found here is used on your own risk.

## Installation
1. Install and configure ESPHome.   Make sure to use the new ESPHome from teh ESPhome repo (https://esphome.io/changelog/2022.2.0.html) rather than Community Repo.
3. Prepare the NSPanel for flashing (see MarkWattTech Video https://youtu.be/p-AK4o5jOSI).
4. Ensure that the ESPhome Secrets are configured with the appropriate SSID, Password, and TFT path.  Use the **secrets.yaml** in repo as an example.    
5. Flash the NSPanel with **nspanel.yaml** "as is" for instalation (We will edit in a bit). Pay special attention to the _tft_url_ parameter and ensure it is accessible by the NSPanel.  Recommend using the www folder in your HA install
6. Download the **HMI.tft** file and save it to the _tft_url_ location.
7. Add the unit to Home Assistant through the ESPHome integration.  (If IP of NSpanel is on smae Network as Home Assisatnt it will automatically be added)
8. Run the _esphome.nspanel_upload_tft_ service from Home Assistant. This will download the HMI to the NSPanel. Please note that this will block the ESPHome connection during the update. Follow the progress on the HMI screen. When the HMI is installed, reboot the unit.
9. Use steps in the Configuration Section below to customize what is being displayed in the LCD

## Configuration
- In the ESPHome Addon Edit the NSPanel Device
- <img width="611" alt="image" src="https://user-images.githubusercontent.com/105226208/167456356-8dd6e3a5-9308-4008-a3f3-abe982b1d067.png">
- Edit the Below Section only
- ![image](https://user-images.githubusercontent.com/105226208/167458091-c9e98dad-b765-484b-994f-215dea04cdb7.png)
- Validate the Config
- ![image](https://user-images.githubusercontent.com/105226208/167515749-e16b8ae7-78ad-47d7-bd06-dc738bcc3c8b.png)

- Install Config Wirelessly
- ![image](https://user-images.githubusercontent.com/105226208/167515817-eac48612-f259-4fe9-ae48-dd9efba9e5b0.png)

## Known Limitations
- Only single page of lights is currently available
- Media Player is CUrrently not working
- Pressing physical buttons does not currenty wake up panel

## To Do's
- Add multiple Page for Lights
- Fix Media Player
- Allow Panel to wake up when Physical buttons are pressed
- Add Additional Icons for the lights Page
- Simplify the chnaging of icons on the light page
