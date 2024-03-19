You can build It: 
https://www.tindie.com/products/6659291/diy-internet-radio-firmware-only/

https://www.ko-fi.com/s/58ace66c90

Only works with ESP32S3 Lilygo t-displayS3 Touch
you can watch the videos:
https://youtu.be/HgioXrjpPSk?feature=shared
https://youtu.be/gyk2eq8ZymM?feature=shared
https://www.youtube.com/watch?v=cFctgusRfhY

The espressif Flash Download Tools can be downloaded from here:
https://www.espressif.com/en/support/download/other-tools

Upload using Espressif Flash Tool
My_Radio.ino  0x0000

![new](https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/67354aed-3f15-427f-bfea-c4d8dc057027)

After ESP32 boot wait for 3 min until network scanning is completed.
Open the wifi in your phone and search for AH_Radio
Connect to your network
Wait for 5 minutes for the Spiff format to be completed
(You might need to turn off/on the radio) Look at the LCD for the IP address
connect to that IP address using your computer browser
Upload a single station or list of stations using the following format

Station Name 1,Station Address 1

Station Name 2,Station Address 2

Radio Ariel,http://123.456.789.0/stream

Radio Hits,http://stream.awesomehitsradio.com
.
You can find station URL's here: https://streamurl.link/
.
Note: The webserver is only working after boot, 
it will stop working once you touch the screen. 
To reactivate it you will need to reboot the radio.

Note: 1. The boot_app0.bin file is included with the Lilygo flash tool in the bin directory.
      2. An I2S DAC is required for this project, Amplifier is optional.  Consult the I2S data sheet to learn how to activate the (L+R)/2 or stereo signal.  

Note: for some stations that don't play and their URL starts with https:// try to change it to http:// and check if it is working

.Connection diagram using the Max98357a chip (if you use a header you don't need to connect wires as the pins are arranged correctly). 
I strongly recommend using the PCM5102a for better sound quality.      
 
Connect the I2S DAC to the following pins: 
BCLK to pin 12, 
LRC to pin 11, 
DOUT to pin 13,
VCC to 5V,
GND to GND

Following is the connection diagram:

![image](https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/d405b0ce-b7a1-45ff-980c-08a1a25e7c60)

Just solder it like that and connect it to the speaker (the pins are already aligned with the DAC pins):

![image](https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/c8c65006-bf70-4d20-8956-596c9431f0fc)


![image](https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/88fd5636-100d-48d0-98b3-11ea5aba370b)


![image](https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/d6fd0191-0bdb-4603-8089-db5a063e00e1)


