# wwhf_2024_badge_notes
As a virtual attendee of WWHF 2024, I was grateful to receive a blank PCB. For the onsite attendees, this was fully built out and used in the fun onsite badge games. Hopefully I can turn this into something useful and learn some new skills along the way!

> [!WARNING] 
> I don't know what I'm doing with most of this... if someone more knowledgeable wants to collaborate, please jump in!

## Notes and questions
* these writeups look useful after we get something soldered together:
   * [ladderlogix/2024-WWHF-Badge-Writeup](https://github.com/ladderlogix/2024-WWHF-Badge-Writeup)
   * [https://github.com/Cooperw/ctf/tree/master/2024-10-11-wwhf24](https://github.com/Cooperw/ctf/tree/master/2024-10-11-wwhf24)
* more reference for learning: [eurofurence/ef28-badge](https://github.com/eurofurence/ef28-badge)
* shout out to 'shilo' from the discord server for providing pictures of the built board!
* everything seems to be surface mount (SMD)
   * [Surface Mount Soldering 101 (video)](https://www.youtube.com/watch?v=3NN7UGWYmBY)
* for display module, I'm assuming they just bent the pins down and soldered to the pads? There seemed to be issues with them falling off from the announcements made.
   * secure with hot glue or think about a different mounting plan
* The official bill of material has been made available from the creator/organizer
   * [Mike Felch (Stay Ready)@ustayready](https://x.com/ustayready)
   * [https://github.com/ustayready/wwhf_2024_badge](https://github.com/ustayready/wwhf_2024_badge)

## Component list
| Component                                                                              |Confidence?    | Documents     | Price guess                                                                                         | Quantity |
| :-------------------------------------------------------------------------------       |:----------:   |:-------------:| --------------------------------------------------------------------------------------------------: | :------  |
| 2024 WWHF PCB (white)                                                                  | send it       | ?             | priceless                                                                                           | 1        |
| 3.7V 1200mAh 603450 Lipo Battery Rechargeable Battery Pack with JST male connection    | getting close |               | [$4](https://www.aliexpress.us/item/2251832678527988.html?gatewayAdapt=glo2usa4itemAdapt)           | 1        |
| ESP32-S3-WROOM-1 with antenna. Not sure on memory size?                                | getting close |               | [$4?](https://www.digikey.com/en/products/detail/espressif-systems/ESP32-S3-WROOM-1-N8R2/15200058)  | 1        |
| JST female connector...                                                                | getting close |               | [but which one](https://www.mattmillman.com/info/crimpconnectors/common-jst-connector-types/)       | 1        |
| 4pin 0.96 inch 128X64 OLED Display Module?                                             | getting close |               | [$3?](https://rainbowsemi.en.alibaba.com/product/60755745658-804119767/4pin_0_96_inch_128X64_OLED_Display_Module_GND_VCC_SCL_SDA_0_96_IIC_Communicate.html) | 1        |
| tactile buttons                                                                        |               |               |                                                                                                     | 2        |        
| USB Type-C Connector                                                                   |               |               |                                                                                                     | 1        |
| nfc tag? Circle/clear                                                                  |               |               |                                                                                                     | 1        |
| bunch of LEDs                                                                          |               |               |                                                                                                     | 1        |
| bunch of resistors                                                                     |               |               |                                                                                                     | 1        |


## Chat GPT's guidance
Just for fun, I was curious how good AI would be at putting this together... it's certainly lining up generically with what I was able to fumble through.

> Based on the image you provided, here’s an attempt to list the full Bill of Materials (BOM) for the PCB. I'll identify the visible components and estimate specifics:
> 
> 1. **ESP32-S3-WROOM-1 Module**
>    - **Description:** A Wi-Fi and Bluetooth module with an ESP32-S3 microcontroller.
>    - **Part Number:** ESP32-S3-WROOM-1-N8 (could be N16 depending on the flash memory size).
>    - **Key Specs:** Dual-core processor, integrated antenna, flash, and RAM.
> 
> 2. **OLED Display (likely 0.96 inch)**
>    - **Description:** A small OLED display for status or information display.
>    - **Part Number:** SSD1306-based OLED module.
>    - **Interface:** I2C (GND, VCC, SCL, SDA connections are labeled).
> 
> 3. **Red LED (Cowboy Eyes)**
>    - **Description:** Two red LEDs for visual effect.
>    - **Specs:** Likely generic 5mm red LEDs.
>    - **Additional Components:** Current-limiting resistors (probably 220Ω to 330Ω).
> 
> 4. **Momentary Push Buttons**
>    - **Description:** Two tactile push buttons for user interaction (A and B labeled).
>    - **Part Number:** Tactile push button (6mm x 6mm).
>    - **Mounting Type:** Through-hole.
> 
> 5. **USB Type-C Connector**
>    - **Description:** USB Type-C connector for power and possibly data.
>    - **Part Number:** Standard USB Type-C receptacle (5-pin).
>    - **Additional Components:** Filter capacitors and resistors for proper connection.
> 
> 6. **Inductive Sensor Coil (Round Coil Near "A")**
>    - **Description:** Likely an inductive sensor for user interaction, possibly part of a capacitive sensing circuit.
>    - **Part Number:** Custom or standard coil.
>    - **Associated Components:** Capacitor and/or inductor for tuning the sensor.
> 
> 7. **Miscellaneous Resistors and Capacitors**
>    - **Description:** Various surface-mount resistors and capacitors for general operation.
>    - **Specs:** 10kΩ, 1kΩ resistors, and 0.1µF decoupling capacitors are likely used.
>    - **Type:** 0805 or 0603 SMD.
> 
> 8. **On/Off Switch**
>    - **Description:** A physical switch for powering the board on or off.
>    - **Part Number:** SPDT slide switch.
> 
> 9. **Battery Connector (JST-type 2-pin)**
>    - **Description:** A connector for external power, likely a LiPo battery.
>    - **Part Number:** JST-PH 2-pin connector.
> 
> 10. **Voltage Regulator**
>     - **Description:** Voltage regulator for stepping down or stabilizing the input voltage (3.3V for the ESP32).
>     - **Part Number:** Likely a 3.3V linear regulator (e.g., AMS1117-3.3).
> 
> 11. **Transistor/IC (Near Switch)**
>     - **Description:** A small IC or transistor, possibly for switching or regulation.
>     - **Specs:** Cannot fully determine from the image, but could be part of power management.
> 
> 12. **Additional LEDs (bottom right)**
>     - **Description:** Red LEDs for indicators or effects, part of the "Official Intergalactic Bounty Association" logo.
>     - **Associated Resistor:** Likely 220Ω or 330Ω current-limiting resistors.
> 
> 13. **Silkscreen Markings & Aesthetic Elements**
>     - **Description:** The PCB also has detailed silkscreen artwork, including a UFO and bounty hunter theme.
> 
> ### Estimate of Other Components:
> - **Crystal Oscillator:** There may be an external crystal oscillator for the ESP32 (if not internal), typically 40MHz.
> - **Decoupling Capacitors:** There are likely multiple 0.1µF capacitors close to power pins for noise reduction.
> - **Inductor (possibly for power regulation):** If there's an inductor, it's part of a buck converter or power supply circuit.
> 
> This is a rough estimate based on what's visible in the image. A full BOM would depend on schematics or a more detailed inspection of the board.


## Rebuild ideas
* contact share-er, like tap to share or receive other nfcs tags. May have to add a reader?
* pong-esque or some other two player one button game
* just a normal tamagotchi
* hash monster
* very light weight piratebox. or even just one way web server.
* pwnagotchi
