# Setting up Home Assistant on a Raspberry Pi 3/4

The easiest way I have seen to do this is to download and install Raspberry Pi Imager (https://www.raspberrypi.com/software/).

## To install Raspberry Pi Imager on Ubuntu, do the following

1. Download the Ubuntu installer from https://www.raspberrypi.com/software
2. Open terminal
3. ```sudo apt install .\imager_%version%_amd64.db``` (change ```%version%``` to the correct version)

## To install Home Assistant on a Raspberry Pi 3 or 4

Note: I am doing this from Ubuntu, but would be similar from Windows and MacOS.

1. Insert microSD card into computer
   1. I read it is recommended to use at least a 64GB microSD card.  However, for this demonstration I am using a 16GB as it should have plenty of space for what we are doing during this presentation.
2. Open Raspberry Pi Imager  
    - ![rpi_Imager_Icon](./images/rpi_imager_icon.png)  
3. Click the "CHOOSE OS" button  
    - ![rpi_Imager_OS](./images/rpi_imager_OS_button.png)  
4. Choose "Other specific-purpose OS" (likely requires scrolling down)  
    - ![rpi_Imager_OS_Menu](./images/rpi_imager_OS_menu.png)
5. Choose "Home assistant and home automation"  
    - ![rpi_Imager_OS_ha_Menu](./images/rpi_imager_OS_ha_menu.png)  
6. Choose "Home Assistant" (likely requires scrolling down)  
    - ![rpi_Imager_OS_ha_Menu2](./images/rpi_imager_OS_menu2.png)  
7. Choose the appropriate option for your model of RPi  
    - ![rpi_Imager_OS_ha_Option](./images/rpi_imager_OS_ha_option.png)  
8. Click the "CHOOSE STOR..." button  
    - ![rpi_Imager_Storage_button](./images/rpi_imager_storage_button.png)  
9. Choose the appropriate device to install to  
    - ![rpi_Imager_Storage_option](./images/rpi_imager_storage_option.png)  
10. Click the "WRITE" button  
    - ![rpi_Imager_write_button](./images/rpi_imager_write_button.png)  
11. Click the "YES" button to agree to continue and overwrite existing data on the card
    - ![rpi_Imager_warning](./images/rpi_imager_warning.png)  
12. You may be required to enter credentials to continue
13. The program will go through a series of step (Downloading, Writing, and Verifying)  
    - ![rpi_Imager_Install](./images/rpi_imager_install.png)  
14. Removed the microSD card from your computer and click "CONTINUE"  
    - ![rpi_Imager_Completed](./images/rpi_imager_completed.png)  
15. Close out of Raspberry Pi Imager as we are done with it

## Initial Configuration Home Assistant

Note: This assumes you have inserted the microSD card into the RPi and connected power, display, and network cable.  Yes, as far as I know, it requires a physical connection to the network to do the initial configuration.  The display isn't required if you aquire the devices IP address from your DHCP server.

1. Power on the Raspberry Pi, if not already powered on, and wait for the CLI to be ready and display an IP address.
2. Open a browser on your computer and go to the IP address listed on the RPi using port 8123.
    - Example: http://192.168.1.250:8123
3. You should see a screen similar to the one below
    - ![HA_prepairing](./images/onboarding_preparing_01.png)  
    - If you want to see the logs as it is starting up, then click the blue animated dot
4. When it is ready enter Name, Username, and Password (twice) and click Create Account  
    - ![HA_create_account](./images/onboarding_create_account.png)  
5. Enter a name for this HA install and either click DETECT or enter Country and Language
    - I would also do the Time Zone, Unit System, and Currency if it didn't populate correctly  
    - ![HA_Location](./images/onboarding_location.png)  
6. Click Next
7. Select what anonymized data you want to send to HA and click NEXT  
    - ![HA_Analytics](./images/onboarding_analytics.png)  
8. You will get a screen showing Devices and Services HA discovered on your network which can be integrated
9. Either set them up by clicking on the ones you want or click FINISH
