# WLED Setup

This will go through how to setup WLED on an esp8266 microprocessor and use it to control WS2815 individually addressable light strip. There are other light strips supported by WLED and other microprocesors WLED will run on.  These are just the ones I selected.  Also note, I am using Ubuntu 22.04.

## Items used

- esp8266 microprocessor
- WS2815 light strip
- 12V power supply (size and voltage dependent on power needed by LED strip chosen)
- Female 12v DC power jack connector

## Flash WLED onto esp8266 board

There are other ways to install WLED, but I used the web installer.  See the [WLED Project site](https://kno.wled.ge/) for other options.

1. From MS Edge or Google Chrome, go to https://install.wled.me/
2. Plug the ESP8266 into a USB port
3. Click the **Install** button
4. Select the proper COM port (mine shows up as TTYUSB0)
5. Click the **Connect** button
6. Click **INSTALL WLED**
7. Click **INSTALL** to agree to install and overwrite existing data
8. Once the _Installation complete_ dialog comes up, click **Next**
9. Now configure Wi-Fi
   1. Enter the SSID in **Network Name**
   2. Enter pre-shared key in **Password**
   3. Click **CONNECT**
10. Proceed to adding to Home Assistant

## Add to Home Assistant

This is assuming you are adding it to Home Assistant directly after flashing WLED to the ESP8266 board and that your computer is on the same Wi-Fi as the ESP8266 board.

1. Click **ADD TO HOME ASSISTANT**
2. Change "homeassistant.local" to the ip or fqdn of your HA install
   1. Should result in something like http://192.168.253.122:8123.
   2. Note, this will only come up if the address of HA is unknown by your browser.
3. Click **SAVE**
4. Click **OPEN LINK**
5. Login to HA using creditials created when installing HA
6. HA should automatically discover WLED and display a dialog asking if you would like to setup WLED.  Click **OK**
7. Click **WLED**
8. Click **SUBMIT**
9. Select an "Area" if you would like to assign the device to a particular area and then click **FINISH**
