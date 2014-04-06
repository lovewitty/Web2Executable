Web2Executable
==============

Uses node-webkit to generate "native" apps for already existing web apps.

Requires the pyside library and python 2.X to run. I've only tested the code on python 2.7.3-2.7.5, so I can't speak about any lower version, but it should work as long as PySide is supported.


Getting Started
---------------

Run with:

```
python main.py
```

It's a pretty simple app. Just point it the the directory that your web application lives, customize the options (the two marked with a star are the only ones required) and then choose your export options. The app will export under YOUR_OUTPUT_DIR/YOUR_APP_NAME. 

What's New?
----------------------

v0.1.3b

- Added the ability to choose node-webkit versions if 0.9.2 is not what you want
- Modified the UI slightly for people with smaller monitors

v0.1.2b

- Fixed an issue with icon copying
- Fixed a bug that overwrote existing package.json files.

Prebuilt Binaries
-----------------

###Mac OS X

[Mac OS X 10.7+ download - v0.1.3b](http://www.mediafire.com/download/xlt355pvl07y029/Web2ExeMac-v0.1.3b.zip)

Previous Version:

[Mac OS X 10.7+ download - v0.1.2b](http://www.mediafire.com/download/uz9aaod7ttvdhyr/Web2ExeMac-v0.1.2b.zip)


You can just put the app where ever you want and double click to run it.

###Windows

[Windows 7+ download - v0.1.3b](http://www.mediafire.com/download/809teb4l93030r4/Web2ExeWin-v0.1.3b.zip)

Previous Version:

[Windows 7+ download - v0.1.2b](http://www.mediafire.com/download/zdnm8y6183215zd/Web2ExeWin-v0.1.2b.zip)


Double click the Win2Exe.exe file inside the extracted folder.

###Linux

Only on Ubuntu 12.04. If someone knows how to make them on all linux distros, let me know. I'm using cx_Freeze to compile them to standalone apps. You must copy all .so.X.X files to either /usr/local/lib/ or /usr/lib/ for it to work.

[Linux 64bit download - v0.1.3b](http://www.mediafire.com/download/2fwb5k3vo2ic371/Web2ExeLinux64-v0.1.3b.zip)

[Linux 32bit download - v0.1.3b](http://www.mediafire.com/download/u46ug222e99a077/Web2ExeLinux32-v0.1.3b.zip)

Previous Version:

[Linux 64bit download - v0.1.2b](http://www.mediafire.com/download/5rm1d68zeyckbde/Web2ExeLinux64-v0.1.2b.zip)

[Linux 32bit download - v0.1.2b](http://www.mediafire.com/download/2rga5pzznnksw0v/Web2ExeLinux32-v0.1.2b.zip)


chmod 755 the Web2Exe binary inside the extracted folder and then run by double clicking or ./Web2Exe from the command line. Also, if you get shared library errors, you need to copy all the .so files into /usr/lib/ or /usr/local/lib/. Make sure you check to see if any libraries in /usr/lib/ conflict with the files first.

```
chmod 755 Web2Exe
sudo cp *.so.* /usr/lib/
```

Note: For some reason, these linux binaries are not working correctly on vanilla systems. I'm looking into the issue and will update them when I figure out what is going on.


Features
--------

Supports exporting web applications to Mac, Linux, and Windows. So far, it works with all the apps I've tested it with. It supports Phaser and I assume it supports all other html5 and javascript libraries because it uses the same engine Google Chrome uses.

Future Features
---------------

- Automatic replacement of icon files inside of Mac apps and Windows exes. Right now, the only way to have a custom Mac icon is to convert your image to .icns format and put it in the resources folder of the app. For windows, you have to use a utility like Resource Hacker.
- Ability to specify a node-webkit version. Currently, it just grabs v0.9.2.

Screenshots
-----------

v0.1.3b

![Screenshot2](http://i.imgur.com/jZ7TE63.png)

v0.1.2b

![Screenshot](http://i.imgur.com/V1609ea.png) 


