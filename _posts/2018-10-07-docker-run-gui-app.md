---
layout:     post
title:      Running GUI applications using Docker in Mac, Linux and Windows
date:       2018-10-07 23:03:19
summary:    How to run GUI applications on MacOs, Linux and Windows
categories: docker
---
Running GUI applications using Docker in Mac, Linux and Windows

## Running On MacOS

Prerequisites:
 - Install XQuartz from https://www.xquartz.org. Installation of XQuartz will require restart your machine.
 - Make sure xhost command is available after the installation
 - Configure XQuartz to `allow connections from network clients` from Preferences -> Security tab

 1- On your local machine, start XQuartz
 2- Run `xhost + ${hostname}` after
 3- Set DISPLAY var in the container: `export DISPLAY=<IP>:0`
 4- Run `xclock` in the container  
 
## Running On Linux
Prerequisites:
 - Install XQuartz from https://www.xquartz.org/
 - Make sure xhost command is available after the installation

To Run:
 1- On your local machine, start XQuartz
 2- Run `xhost + ${hostname}` in the local machine
 3- Set DISPLAY var in the container: `export DISPLAY=<IP>:0.0`
 4- Run `xclock` in the container  

## Running On Windows
Prerequisites:
 - Install VcXsrv Windows X Server (https://sourceforge.net/projects/vcxsrv/) manually  or `choco install vcxsrv`
 - Run Xlaunch from the start menu and perform the initial configuration. 
 - Make sure to save to configuration file before you click finish. Save it to one of the following locations:
	```
    %appdata%\Xming
	%userprofile%\Desktop
	%userprofile%
    ```
1- Run Xlaunch
2- Find up by `ipconfig` on the local machine
3- Set DISPLAY var in the container: `export DISPLAY=<IP>:0.0`
4- Run `xclock` in the container  
