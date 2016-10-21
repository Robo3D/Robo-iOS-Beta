# Robo-iOS-Beta
#### A place for iOS development of the Robo App

## Getting started with Octoprint

The easiest way to get started with Octoprint is Octopi, a ready-made image for the Raspberry Pi.  To get this image, simply download it here: https://octopi.octoprint.org/latest

### Getting Started with OctoPi
Once you have downloaded the image from above, you will need to write the image to an SD card.  If you don't know how to do that, you can find the instructions below.  If you're already comfortable with writing Raspberry Pi images, follow these next steps:

1.   Configure your WiFi connection by editing octopi-network.txt on the root of the flashed card when using it like a thumb drive.  
Boot the Pi from the card.

2.  Log into your Pi via SSH (it is located at octopi.local if your computer supports bonjour or the IP address assigned by your router), default username is “pi”, default password is “raspberry”. Change the password using the passwd command and expand the filesystem of the SD card through the corresponding option when running sudo raspi-config.

3.  Access OctoPrint through http://octopi.local or http://<your pi's ip address>.


### Connecting the Robo app to Octoprint

Setting up the Robo app to talk to your printer is easy, just follow the screenshots below.

#### Step 1: Select "ADD A PRINTER" from the Dashboard screen





#### Step 2: Select "Scan for Printer Name / IP" 
This will automatically fill out the printer name and IP address.  If this does not work, enter the IP address manually and give your printer a name.

#### Step 3: Scan your printer's QR code under "Settings" and "API" - the QR code reader will populate the required field.  Press "Use Key" to finish this step.

#### Step 4: Complete the setup by pressing "Add Printer" at the bottom of the screen.
