# EJ253 ECU Replacement Project - 2026?

## Thesis statement
Here's the background, I have an [Ice Racer](https://www.casc.on.ca/ice-racing-about) that is down to one key, and it doesn't appear possible to be possible to run without the ABS working. It goes into the limp mode in the attempts I've made. I am also driving with only the valet key. I believe replacing the ECU will give me better control over throttle response, eliminate the lost key issue, and allow complete ABS removal and replacement.

<img width="3104" height="1746" alt="image" src="https://github.com/user-attachments/assets/b34888c4-36e2-4424-a177-05c4789546fa" />

I selected a [rusEFI](https://rusefi.com/) replacement ECU because of cost and features. Well, I hope it has the right features, I selected the [uaEFI PRO](https://wiki.rusefi.com/uaEFI/) with molex and WBO cable kit. 

## Pinout
I did a quick test with AI about the pinout compatibility, but now I need to do the work and learn how the connections will work. 

| uaEFI Pin | uaEFI Pigtail Colour | uaEFI Description | Description | Subaru Connector | Subaru Pin |
| --- | --- | --- | --- | --- | --- |
| A1 | white | etb (DC1-) | **Electronic Throttle Body (-)** | | |
| A2 | white | etb (DC2-) | | | |
| A3 | black | gnd (Power Ground) | | | |
| A4 | black | gnd (Power Ground) | | | |
| A5 | blue  | etb (DC1+) | **Electronic Throttle Body (+)** | | |
| A6 | blue  | etb (DC2+) | | | |
| A7 | red   | Ignition SW / Batter Voltage Analog Input | | | |
| A8 | red   | +12V From Main Relay | | | |

