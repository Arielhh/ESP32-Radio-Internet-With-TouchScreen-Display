
![WOW (1)](https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/c3e2c1ed-ae2e-4ef1-8c4e-736ea6311608)




Only works with ESP32S3 Lilygo t-displayS3 Touch
you can watch the videos:
https://youtu.be/HgioXrjpPSk?feature=shared
https://youtu.be/gyk2eq8ZymM?feature=shared

Upload using Espressif Flash Tool
0x0 touchSlider100.ino.bootloader.bin
0x8000 touchSlider100.ino.partitions.bin
0xe000 boot_app0.bin
0x10000 touchSlider100.ino.bin


![WhatsApp Image 2023-09-01 at 13 55 48](https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/db2f634a-4fb8-4936-bf85-d655123cbe20)

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

.
Connect the I2S DAC to the following pins:
#define I2S_BCLK 12
#define I2S_LRC 11
#define I2S_DOUT 13


/*ESP32S3*/
#define PIN_LCD_BL 38

#define PIN_LCD_D0 39
#define PIN_LCD_D1 40
#define PIN_LCD_D2 41
#define PIN_LCD_D3 42
#define PIN_LCD_D4 45
#define PIN_LCD_D5 46
#define PIN_LCD_D6 47
#define PIN_LCD_D7 48
#define I2S_BCLK 12
#define I2S_LRC 11
#define I2S_DOUT 13

#define PIN_POWER_ON 15

#define PIN_LCD_RES 5
#define PIN_LCD_CS 6
#define PIN_LCD_DC 7
#define PIN_LCD_WR 8
#define PIN_LCD_RD 9

#define PIN_BUTTON_1 0
#define PIN_BUTTON_2 14
#define PIN_BAT_VOLT 4

#define PIN_IIC_SCL 17
#define PIN_IIC_SDA 18
#define PIN_TOUCH_INT 16
#define PIN_TOUCH_RES 21

Connection diagram using the Max98357a chip (if you use a header you don't need to connect wires as the pins are arranged correctly). 
I strongly recommend using the PCM5102a for better sound quality.      
 
 
Connect the I2S DAC to the following pins: 
BCLK to pin 12, 
LRC to pin 11, 
DOUT to pin 13,
VCC to 5V,
GND to GND

Following is the connection diagram:

https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/01d28d65-6a7c-488d-b9be-5a0989937efb

https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/ba58d639-86a4-468c-be40-080cd5bb06d6

https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/7131c6dc-841c-486b-a339-76b004c29bfc

https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/c0c5554b-e625-47fc-b1f9-4bbbfa024bc4

![image](https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/d6fd0191-0bdb-4603-8089-db5a063e00e1)


