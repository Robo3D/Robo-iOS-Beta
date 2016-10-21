# Robo-iOS-Beta
#### A place for iOS development of the Robo App

### How to report bugs
Bugs can be reported either in the "Issues" tab above (this is the preffered way), or email us the details at beta@robo3d.com

## Getting started with Octoprint

The easiest way to get started with Octoprint is Octopi, a ready-made image for the Raspberry Pi.  To get this image, simply download it here: https://octopi.octoprint.org/latest

### Getting Started with OctoPi
Once you have downloaded the image from above, you will need to write the image to an SD card.  If you don't know how to do that, you can find the instructions below.  If you're already comfortable with writing Raspberry Pi images, follow these next steps:

1.   Configure your WiFi connection by editing octopi-network.txt on the root of the flashed card when using it like a thumb drive.  
Boot the Pi from the card.

2.  Log into your Pi via SSH (it is located at octopi.local if your computer supports bonjour or the IP address assigned by your router), default username is “pi”, default password is “raspberry”. Change the password using the passwd command and expand the filesystem of the SD card through the corresponding option when running sudo raspi-config.

3.  Access OctoPrint through http://octopi.local or `http://<your pi's ip address>.`


#### Connecting the Robo app to Octoprint.

Setting up the Robo app to talk to your printer is easy, just follow the steps below.

#### Step 1: Select "ADD A PRINTER" from the Dashboard screen

#### Step 2: Select "Scan for Printer Name / IP".
This will automatically fill out the printer name and IP address.  If this does not work, enter the IP address manually and give your printer a name.

#### Step 3: Scan your printer's QR code under "Settings" and "API". 
The QR code reader will populate the required field.  Press "Use Key" to finish this step.

#### Step 4: Complete the setup by pressing "Add Printer" at the bottom of the screen.

## Flashing the image to your SD Card

### Windows

1. Download Win32 Disk Imager from here http://win32-disk-imager.en.lo4d.com/  and open up the program
2. Warning: CHECK this step very CAREFULLY - Click on the device you want to write to (hint; make sure its your sd card) you do not     want to overwrite your hard drive with all of your other files on it
3. Click on the folder icon to select your image file
4. Find the robo file and click open
5. Double check to make sure you are writing the file to the right sd card
6. Click "Write"
7. Click "Yes"
8. Eject the sd card safely to avoid curruption

### Mac

#### Format your sd card
1. Insert the sd card into your mac
2. Search 'disk utility' in upper right corner of your desktop search function
3. In the left column, click on the sd card you just inserted (note: DO NOT click on your other hard drives, as it can erase all of your    data on your computer. Make sure you select the sd card you just inserted)
4. In the main window click on the second tab 'erase',
5. Go to the format drop down; it should be selected as MS-DOS (FAT)
6. Click 'erase' button to format the disk
7. Close disk utility
8. Take out sd card

#### Flash disk image

1. Search 'Terminal' in the upper right corner of your desktop search function
2. Once terminal is open type df -h
		This will bring up a list all of the drives that are on your system
3. Insert the sd card back into your computer
4. Again, type in df -h
	You should see a list of the drives on your system but also one more drive that is your sd card (example name of my sd card is 		disk1s1, but yours could be something with a different name)
5. Type in diskutil unmount /dev/disk1s1 (disk1s1 is the name of my sd card but yours could be different so replace disk1s1 with the 		name of your sd card that you saw in the last step)
6. From here on out, replace the name of your sd card with rdisk1 (this means put an r in front of disk, and take off the s1 at the end) 	this will make sense in the next step)
7. Type in dd bs=4M status=progress if=~/desktop/imagename.img of=/dev/rdisk1 (replace /desktop/imagename.img with the path of where 		your image is saved (I saved mine to the desktop), and replace disk1s1 with the new name rdisk1)
		
#####Or
		
Download PiWriter from here, https://sourceforge.net/projects/piwriter/files/PiWriter-2.x/ and write the image to your sd from the application. Tutorial video found here, https://youtu.be/PIvNxprbDhQ

