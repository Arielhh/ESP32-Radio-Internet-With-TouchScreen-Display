ESP32S3 Lilygo t-displayS3 Touch

The espressif Flash Download Tools can be downloaded from here:
https://www.espressif.com/en/support/download/other-tools

Upload using Espressif Flash Tool
0x0 touchSlider100.ino.bootloader.bin
0x8000 touchSlider100.ino.partitions.bin
0xe000 boot_app0.bin
0x10000 touchSlider100.ino.bin

After ESP32 boot wait for 3 min until network scanning is completed.
Open the wifi in your phone and search for AH_Radio
Connect to your network
Wait for 5 min for the Spiff format to be completed
Look at the LCD for the IP address
connect to that Ip Address using your computer browser
upload single station or list of stations using the following format

Station Name 1,Station Address 1
Station Name 2,Station Address 2

Radio Ariel,http://123.456.789.0/stream
Radio Hits,http://stream.awesomehitsradio.com
.
You can find station URL's here: https://streamurl.link/ 
.
Connect the I2S DAC to the following pins:
#define I2S_BCLK 12
#define I2S_LRC 11
#define I2S_DOUT 13

Note: 1. The boot_app0.bin file is included with the Lilygo flash tool in the bin directory.
       2. An I2S DAC is required for this project, Amplifier is optional.  Consult the I2S data sheet to learn how to activate the (L+R)/2 or stereo signal.  
Note: for some stations that doesn't play and starts with https:// try to change to http:// and check if it is working
