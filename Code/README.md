# Code Modifications

Thhis folder contains a necessary file that needs to be copied over the existing one in Meshtastic (SX1278.cpp) and two optional ones
that provide further performance increases for the SX1276 chip (SX1276.cpp and BuildOptUser.h).

These files should be copied over the existing files in the directory for node before compiling the code.
For example the existing pinout shown in the Reference Schematic will work with the T-Beam variant. 
So in the PlatformIO\Projects\firmware\.pio\libdeps\tbeam\RadioLib\src\modules\SX127x\ folder you would paste the SX1278.cpp and SX1276.cpp files.
Then in the PlatformIO\Projects\firmware\.pio\libdeps\tbeam\RadioLib\src\ folder you would paste the BuildOptUser.h file.
Then compile the firmware.

The change in SX1278.cpp is needed to tell the SX1276 IC which RF output pin to use. Without this change there will be no output from the module