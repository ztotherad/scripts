# My Personal Scripts
These are my personal scripts. Feel free to modify/steal/call yours, I don't care.

## Script information
### **build**
This is simply a script that automatically builds all of my ROMs. It also shortens up some of the longer 
commands used when building, such as `repo sync -j6 --no-tags --no-clone-bundle --force-sync -f -q`,
it also uploads them to gdrive automatically.

### **buildid**
This script just grabs the build id and release key from the system.img in the factory image.
To use it, put the script in the same directory as the system.img from the factory
image, then simply type `./buildid` in the terminal. It will ask you for the superuser password, this
is because it has to mount the system.img to access what is inside of it.

## **getimages**
This script downloads the factory image and extracts the bootloader, radio, and vendor image from it.
After it extracts the images, it copies them to wherever you set `$savedir` and adds your device and the month/year
to the name of the images.
After everything is configured, Here is how you use it. The syntax of the command is `./getimages <url-of-factory-image>` To get the factory image url, just goto 
googles factory image page and copy the download link by right clicking `link` on the factory image you want to download.

## **getblobs**
This script is a modified version of Myself5's getblobs script. It is a script used to grab to grab a factory image and extract it, that way it is ready to extract the vendor blobs 
from it.
usage: `./getblobs <url-of-factory-image>`. You can also use `./getblobs <url-of-factory-image> -r` for ROM's that do not support setting the correct platform signature on vendor 
packages. Adding `-r` will just copy the contents of **vendor** to **system/priv-app**.
