# Robo-iOS-Beta
#### A place for iOS development of the Robo App

## Getting started with Octoprint

The easiest way to get started with Octoprint is Octopi, a ready-made image for the Raspberry Pi.  To get this image, simply download it here: https://octopi.octoprint.org/latest

### Getting Started with OctoPi
Once you have downloaded the image from above, you will need to write the image to an SD card.  If you don't know how to do that, you can find the instructions below.  If you're already comfortable with writing Raspberry Pi images, follow these next steps:
```
Configure your WiFi connection by editing octopi-network.txt on the root of the flashed card when using it like a thumb drive.  
Boot the Pi from the card.
```
```
Log into your Pi via SSH (it is located at octopi.local if your computer supports bonjour or the IP address assigned by your router), default username is “pi”, default password is “raspberry”. Change the password using the passwd command and expand the filesystem of the SD card through the corresponding option when running sudo raspi-config.
```
```
Access OctoPrint through http://octopi.local or http://<your pi's ip address>.
```
