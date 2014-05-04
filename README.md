# Pacman Adventures #

This is an example C++ application using the SDL library.
It tries to be as nicely C++11 as possible but do keep in
mind that SDL is written in C and, at some stage, you have
to interface with it.

## Story ##
You play as pacman, a devious little ball whos only goal is to eat oranges and find cherrys on the map. Weeve through the map as you find all the collectibles and dodge walls. 

## Installation ##
This game was developed using a Virtual Machine for Fedora 20, on a Windows 8.0 system. You will have to have the SDL development libraries installed on your system in order to execute my game.  The easiest way to do this, would be through the terminal.

First, you'll need to install the SDL library. The first two lines will allow you to download GCC compiler and C++ database. The third line installs mesa drivers from the SDL library, which will help with graphical drivers. 

`$ su -l`

`$ sudo yum groupinstall “Developemnt Tools”`

`$ sudo yum install SDL*`

Navigating to your forked /src/ folder:
`$ cd /home/ivan/University/CI123/StarshipFontana-master/src`

Don't forget! To speed up the process of typing out the whole commandline, you can just type the first letter followed by pressing tab to flick through all the various folders.

Next, you'll need execute the flags that are located in your /src/ folder. These two command lines will help you create the object files:

`$ g++ -c -std=c++0x Main.cpp SFApp.cpp SFAsset.cpp SFBoundingBox.cpp SFEvent.cpp`

`$ g++ -o pacman Main.o SFApp.o SFAsset.o SFBoundingBox.o SFEvent.o -lSDL -lSDL_image`

Finally, typing the following will allow you to run the game:

`$ ./pacman`

If you ever run into issues with the game, repeat the process carefully. You can delete your objects and pacman application with the following commands:

`$ rm *.o`
`$ rm pacman`


 
## Credits ##
The sprites used in this game fall under the Fair Use Copyright Act, which allow me to use the images in my game, for non-commercial and educational purposes. If you wish to find out more, please visit [Copyright Services](http://www.copyrightservice.co.uk/copyright/p09_fair_use)
