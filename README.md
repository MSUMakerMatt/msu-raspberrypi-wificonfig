Configuration files for Raspbian in order to connect Raspberry Pi microcomputers to the MSU-Secure Network at Montana State Unversity in Bozeman, Montana.


**Instructions**

*Prerequisites*: 

* Raspberry Pi 3 or newer or Raspberry Pi Zero or Zero W
* MicroSD Card with latest Raspbian Desktop OS flashed

1. Boot Raspberry Pi and open a File Manager window
2. Navigate to /etc/network and paste interfaces into the folder, overwriting the existing interfaces file.
3. Navigate to /etc/wpa_supplicant and paste the wpa_supplicant file into the folder, overwriting the existing file
4. Open a Terminal window and type the following: 'echo -n password | iconv -t utf16le | openssl md4'. Replace password with your NetID Password.
5. Copy the the resulting has by double clicking on the hash, then right clicking once, then selecting copy.
6. Open the wpa-Supplicant.conf file and paste the hash after the colon on line 10.
11. Replace "netID" on line 9 with your NetID in quotation marks, ie. "a12b345".
12. Save the file and reboot your Raspberry Pi.

You should now have access to the secure network. 

If you have any problems, please open an issue!
