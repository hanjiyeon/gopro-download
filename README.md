gopro-download
==============

A simple (one class) java app to download all files from your [wifi-enabled GoPro](http://gopro.com/hd-hero3-cameras) camera.
It does a "does the file exist" check to skip previously downloaded files, so if you want to re-download, move the previous images and videos to another folder.
All files are dropped off in your UserHome/Pictures/gopro folder, which for most OSs, is the regular folder for pictures and videos.

Building:
```
git clone https://github.com/salamanders/gopro-download
ant jar
java -jar ./dist/gopro-download.jar
```

Usage:

* If you have a GoPro HERO3 Black with firmware 03.00, After July 31, you can use the software now.
* But, if you have a HERO3 Black with firmware BELOW 03.00, you need to add a file to your sd card and restart the gopro. [Read Why](http://pocket-lifestyle.tumblr.com/hd3_black_tutorial)  The file is at [autoexec.ash](https://raw.github.com/salamanders/gopro-download/master/src/autoexec.ash) which you can right-click and save to the card's root.
* If you have a HERO3 White/Silver, thats OK, use the software right now.
* Turn on your camera's wifi in the "gopro app" control mode.
* Connect your PC (any OS) to the camera's wifi network.  If you don't know the password, try "goprohero"
* Make sure you are connected by trying to open http://10.5.5.9:8080/
* If you are confident, run the jar by double-clicking.  If first time, you may want to run from the command line (as shown above) to watch the output.


TODO:

- [*] Python version for the noJava people
- [ ] Handle if there is pagination
- [ ] Delete files from the GoPro once checked that they downloaded safely
