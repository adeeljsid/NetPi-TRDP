                                                               
                  _____ _____ ____  _____    _____ _____ __ __ 
                 |_   _| __  |    \|  _  |  |   __|  _  |  |  |
                   | | |    -|  |  |   __|  |__   |   __|_   _|
                   |_| |__|__|____/|__|     |_____|__|    |_|  
                                                               

															   
This Plugin can be used to display packages containing TRDP (Train Realtime Data Protocol).

The Plugin was developed for wireshark version 1.8.3.

B U I L D I N G
===============

For Windows:
	build.bat

The file must probalby be adapted to the installed Visual-Studio Version.
The in the file clean.bat, the installed visual studio version must also be set.


For Linux:
	Makefile

If not already done, libxml2 must be installed as development version on the host.

Example for Ubuntu step by step:
 cd <this directory>
 sudo aptitude install libxml2-dev
 sudo aptitude install wireshark-dev
 export WIRESHARK_SRC=/usr/include/wireshark
 make
 sudo cp packet-trdp_spy.so "/usr/lib/$(uname -m)-linux-gnu/wireshark/libwireshark3/plugins/"
 
C L E A N
=========

For Windows:
	clean.bat
	
For Linux:
	make clean
