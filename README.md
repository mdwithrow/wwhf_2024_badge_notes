# wwhf_2024_badge_notes
As a virtual attendee of WWHF 2024, I was grateful to receive a blank PCB. For the onsite attendees, this was fully built out and used in the fun onsite badge games. Hopefully I can turn this into something useful and learn some new skills along the way!

⚠️ I don't know what I'm doing with most of this... if someone more knowledgeable wants to collaborate, please jump in!⚠️

## Notes and questions
* these writeups look useful after we get something soldered together:
   * [ladderlogix/2024-WWHF-Badge-Writeup](https://github.com/ladderlogix/2024-WWHF-Badge-Writeup)
   * [https://github.com/Cooperw/ctf/tree/master/2024-10-11-wwhf24](https://github.com/Cooperw/ctf/tree/master/2024-10-11-wwhf24)
* more reference for learning: [eurofurence/ef28-badge](https://github.com/eurofurence/ef28-badge)
* shout out to shilo from the discord server for providing pictures of the built board!
* everything seems to be surface mount (SMD)
* for display module, I'm assuming the just bent the pins down and soldered to the pads? There seemed to be issues with them falling off from the announcements made. 

## Component list
| Component                                                                              |Confidence?    | Documents     | Price guess                                                                                         | Quantity |
| :-------------------------------------------------------------------------------       |:----------:   |:-------------:| --------------------------------------------------------------------------------------------------: | :------  |
| 2024 WWHF PCB (white)                                                                  | send it       | ?             | priceless                                                                                           | 1        |
| 3.7V 1200mAh 603450 Lipo Battery Rechargeable Battery Pack with JST male connection    | getting close |               | [$4](https://www.aliexpress.us/item/2251832678527988.html?gatewayAdapt=glo2usa4itemAdapt)           | 1        |
| ESP32-S3-WROOM-1 with antenna. Not sure on memory size?                                | getting close |               | [$4?](https://www.digikey.com/en/products/detail/espressif-systems/ESP32-S3-WROOM-1-N8R2/15200058)  | 1        |
| JST female connector...                                                                | getting close |               | [but which one](https://www.mattmillman.com/info/crimpconnectors/common-jst-connector-types/)       | 1        |
| 4pin 0.96 inch 128X64 OLED Display Module?                                             | getting close |               | [$3?](https://rainbowsemi.en.alibaba.com/product/60755745658-804119767/4pin_0_96_inch_128X64_OLED_Display_Module_GND_VCC_SCL_SDA_0_96_IIC_Communicate.html) | 1        |
| tactile buttons                                                                        |               |               |                                                                                                     |          |        
| toggle switch                                                                          |               |               |                                                                                                     |          |        


## Rebuild ideas
* contact share-er, like tap to share or reieve other nfcs tags. May have to add a reader.
* pong 
* just a normal tamagotchi
* wifi pwnagotchi
