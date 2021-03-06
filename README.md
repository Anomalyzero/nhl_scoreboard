# nhl_scoreboard
NHL Scoreboard project for use with Raspberry Pi. This project was shamelessly forked for use in a gift for a family member.
The project uses arim215's NHL Goal Light project as a backbone, and expands it by allowing control of 2 Seven Segment displays like [these](http://www.kingbrightusa.com/product.asp?catalog_name=LED&product_id=SA40-19EWA).

These displays need more current (and voltage) than the maximum 57ma that can be provided by the GPIO, so a custom circuit is needed to control the displays via the GPIO. This circuit uses transistors to provide current from a larger supply. A circuit schematic will be added soon.

The rest of this README document is the original from arim215's project. Later, I will clean up this README and make it more specific to this project. Or I'll forget about it ¯\_(ツ)_/¯

[![GitHub release](https://img.shields.io/github/release/arim215/nhl_goal_light.svg)](https://github.com/arim215/nhl_goal_light/releases)
[![closed pull requests](https://img.shields.io/github/issues-pr-closed/arim215/nhl_goal_light.svg)](https://github.com/arim215/nhl_goal_light/pulls?q=is%3Apr+is%3Aclosed)
[![Libraries.io for GitHub](https://img.shields.io/librariesio/github/arim215/nhl_goal_light.svg)](https://github.com/arim215/nhl_goal_light/blob/master/requirements.txt)
[![license](https://img.shields.io/github/license/arim215/nhl_goal_light.svg)](https://github.com/arim215/nhl_goal_light/blob/master/LICENSE)

## Overview

Nhl goal light python3 for raspberry pi GPIO. Works with any team, just enter team **name without city** when prompted.

Before use, make sure you have:

Python3, python3-pip, mpg123, git

Run the following commands manually to install requirements

run:

    $ sudo apt-get install git mpg123 python3 python-pip3
    $ sudo git clone https://github.com/arim215/nhl_goal_light.git 
    $ sudo pip3 install -r requirements.txt
        

You can prepare a "settings.txt" file to auto-config the nhl_goal_light.py code, or the code will ask for your input everytime.

To start application, use following commands:
	
    $ sudo python3 nhl_goal_light.py

***
### Materials

For documentation on how to wire the GPIOs with the lights and the button, pleaser refer to the "docs" folder.

* Raspberry Pi (currently using raspberry pi A model, but any model will work)
* Red Rotating Beacon Warning Light from ebay
* 5V 2 Channel Relay Module from ebay
* Momentary OFF ON Push Round Button
* 12V to 5V 1A adapter (used a car usb adapter) would be good to have a dual usb adapter in case you need to plug something else like a usb speaker.
* 3.5mm audio extension cable

***
### Audio

If you wish to change the audio clips to sounds with your teams goal horn and music, just download them, rename them (goal_horn_#.mp3) and save them in the "audio" folder.

***
### Delay

I've teste my code while watching Rogers Gamecenter Live and the stream seems to be a bit delayed, so I added a delay to my code to make the goal horn start later. You will be prompted to enter a delay that works with your stream.
