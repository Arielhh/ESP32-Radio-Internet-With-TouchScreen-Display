


![IMG_3577](https://github.com/user-attachments/assets/19e128bc-b9b6-4e2b-bd15-aea5ab638663)

![IMG_3576](https://github.com/user-attachments/assets/ca0a1ff1-3cd8-4685-a9a8-28e3d01f89e3)

Email me if you have any questions: themicromaker@outlook.com

This is a fully functional Internet Radio Based on ESP32-S3

Important Note: To enable the sound it is required to purchase a license key

Note: The Radio was designed to work only with ESP32S3 Lilygo t-displayS3 Touch or an ESP32-S3 and 170x320 touch screen that share the same caracteristics


You can watch the Radio V1 and V4/5 youtube videos here:

https://www.youtube.com/watch?v=8kRRnhr_VSs

https://youtu.be/HgioXrjpPSk?feature=shared

https://youtu.be/gyk2eq8ZymM?feature=shared

https://www.youtube.com/watch?v=cFctgusRfhY

My repository: https://tinyurl.com/4yduvmdj

<img width="228" height="228" alt="image" src="https://github.com/user-attachments/assets/e6c9b7a2-3e71-4442-8183-ced2320a94c2" />

There is also a Bluetooth version without ann internal speaker:


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





There is also a bluetooth version (without a speaker):
![IMG_4067](https://github.com/user-attachments/assets/a20ece25-72aa-4b3f-93ca-11b82eedc690)

![IMG_E4071](https://github.com/user-attachments/assets/1cafccae-8f19-4aa5-95db-807c45a0d5f8)

you can watch the video here:


[![▶ Watch the video](https://img.youtube.com/vi/UsdidMPg164/hqdefault.jpg)](https://youtu.be/UsdidMPg164)


[![▶ Watch the video](https://img.youtube.com/vi/jb2SspnF-nk/hqdefault.jpg)](https://youtu.be/jb2SspnF-nk)



<img width="960" height="2079" alt="IMG_4120" src="https://github.com/user-attachments/assets/25ca0843-2f65-4cc2-a37c-2d5a26b93e64" />


<img width="960" height="2079" alt="IMG_4119" src="https://github.com/user-attachments/assets/05e602a6-6c70-4f35-9cd4-3f1f6bd80f06" />


<img width="960" height="2079" alt="IMG_4118" src="https://github.com/user-attachments/assets/533ca806-4d90-4311-9fdc-9479be0be163" />


<img width="960" height="2079" alt="IMG_4117" src="https://github.com/user-attachments/assets/ed21bb34-0ba5-46ee-ae3a-978e6f882bd2" />


<img width="960" height="2079" alt="IMG_4116" src="https://github.com/user-attachments/assets/d86291b0-c3cf-4f3c-a790-0854d6250496" />













