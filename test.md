
- []()



### Loading and Unloading Wireless Drivers
- Determine our device's driver
```
sudo airmon-ng
```
-  Lists a system's USB devices and shows detailed information for each device:
```
sudo lsusb -vv
```

### Wireless Tools
- iwconfig manipulates the basic wireless parameters: change modes, set channels, and keys.
- iwlist allows for the initiation of scanning, listing frequencies, bit rates, and encryption keys.
- iwspy provides per-node link quality (not often implemented by drivers).
- iwpriv allows for the manipulation of the Wireless Extensions specific to a driver.

### The iw Utility

Provide lots of information about the wireless devices and their capabilities
```
sudo iw list
```
To get a listing of wireless access points that are within range of our wireless card, we will use iw with the dev wlan0 option, which specifies our device. Next, we'll add the scan parameter. We then pipe this command through grep SSID to filter our output to only wireless network names
```
sudo iw dev wlan0 scan | grep SSID
```

