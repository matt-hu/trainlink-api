# TrainLink API 0.1.0
 This is an API to intergrate with a DCC++ (or DCC++ EX) BaseStation. It provides a simple way to control it over your local network, with multiple instances supported. This means if you open a website using TrainLink on two devices connected to the same server, they will be kept in sync!

 ## What is in this Repository?
 In this repository you will find the following (the sublist shows supported platforms, whilst ones in italic are planned for the future):
* The API Server
    * Python (Cross-platform)
    * _Arduino (ESP32/ESP8266)_
* The API Library
    * Javascript (Cross-platform)
    * _Arduino_
    * _Python_
* A Demo page

## Why should I use TrainLink?
One of the major features of trainlink is the cross-platform nature of the API. The server runs on Python, meaning it can be run on most platforms. Also, the API library is written in Javascript, so again, it can be run on most platforms.

Also, TrainLink is very flexible to different development styles. For example, if you don't need the sync feature, you can just send direct commands.

## Getting Started
### What you need to install
1. First, you need to download the latest version of the API from this repository from the releases section (for more information, see the _Releases and Branches_ section below)
1. After that, to run the server you will need Python installed on your PC. The latest version of Python is recommended, versions 3.7 and 3.8 have been tested. However, this is not to say other versions won't work. You can download Python [here](https://www.python.org/downloads/).  
__Note:__ When installing Python, make sure to check 'Add Python to Path'
![How to enable add python to path](/documentation/images/install-python-path.jpg)

1. Next, you need to install the required packages that the server needs. These are:
    * [Websockets](https://websockets.readthedocs.io/en/stable/index.html)
    * [Serial](https://pyserial.readthedocs.io/en/latest/index.html)  

    These can be installed via _reqirements.txt_, or alternativly via pip individually. To use _requirements.txt_, change into the directory where you downloaded the release then run:
    ```console
    $ pip install -r requirements.txt
    ```
1. Your TrainLink installation is done! If you want to try out the demo page, start by running the server, then go into the Demo Pages folder

## What features are supported?
For the full list of supported features and commands, please see the wiki and full documentation. Here is a brief list of what is currently __fully__ supported or planned:
Feature | Version
--------|--------
Cab control | 0.1
Track power control | 0.1
Direct command | 0.1
_Cab functions_ | _0.2_

The reason I say fully supported is because the API has the direct command function. This allows DCC++ comands (such as `<t 1 3 126 1>`) to be sent directly to the base s tation, so all DCC++ commands are supported to some degree. Full support means they are handled by the server and are synced between instances.
