


![IMG_3577](https://github.com/user-attachments/assets/19e128bc-b9b6-4e2b-bd15-aea5ab638663)




This is a fully functional Internet Radio Based on ESP32-S3

Note: it was designed to work only with ESP32S3 Lilygo t-displayS3 Touch or an ESP32-S3 and 170x320 touch screen that share the same caracteristics

You can watch the youtube videos here:
https://youtu.be/HgioXrjpPSk?feature=shared

https://youtu.be/gyk2eq8ZymM?feature=shared

https://www.youtube.com/watch?v=cFctgusRfhY

My repository: https://1drv.ms/f/c/38ba1975d40552d7/EtdSBdR1GboggDh6AAAAAAABXGewSTWX4JG938piuGl--g

The espressif Flash Download Tools can be downloaded from here:
https://www.espressif.com/en/support/download/other-tools

Uploading the firmware is done using the Espressif Flash Tool
My_Radio.ino  0x0000

![new](https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/67354aed-3f15-427f-bfea-c4d8dc057027)

After ESP32 boot wait for few min until network scanning is completed.
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
![2000](https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/eb7a9487-50be-4602-b988-5af08c9675d4)

Just solder it like that and connect it to the speaker (the pins are already aligned with the DAC pins):


![2001](https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/cfae9a96-6d9e-48fd-bd41-e1cd02ca62a5)


![image](https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/d405b0ce-b7a1-45ff-980c-08a1a25e7c60)
![image](https://github.com/Arielhh/ESP32-Radio-Internet/assets/4849568/d6fd0191-0bdb-4603-8089-db5a063e00e1)

Optional Pam8406 amplifier 2x6w amp+ pcm5102a Stereo DAC on one PCB which can be mounted directlly on top of the LILYGO T-Display Touch S3 (no wires soldering needed)
![pam](https://github.com/user-attachments/assets/7c26c655-e0bc-49e2-af36-5a40c3ad6195)

![2024-06-06T10_59_08 115Z-WhatsApp Image 2024-06-06 at 12 58 08_e0c1f9cc (1)](https://github.com/user-attachments/assets/121381f5-67da-4633-869a-6491bd0f7263)
