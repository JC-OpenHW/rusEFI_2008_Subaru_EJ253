# EJ253 ECU Replacement Project - 2026?

## Thesis statement
Here's the background, I have an [Ice Racer](https://www.casc.on.ca/ice-racing-about) that is down to one key, and it doesn't appear possible to be possible to run without the ABS working. It goes into the limp mode in the attempts I've made. I am also driving with only the valet key. I believe replacing the ECU will give me better control over throttle response, eliminate the lost key issue, and allow complete ABS removal and replacement.

<img width="3104" height="1746" alt="image" src="https://github.com/user-attachments/assets/b34888c4-36e2-4424-a177-05c4789546fa" />

I selected a [rusEFI](https://rusefi.com/) replacement ECU because of cost and features. Well, I hope it has the right features, I selected the [uaEFI PRO](https://wiki.rusefi.com/uaEFI/) with molex and WBO cable kit. 

## Pinout
I did a quick test with AI about the pinout compatibility, but now I need to do the work and learn how the connections will work. 

*Current Status: Working on the rusEFI side*

| uaEFI Pin | uaEFI Pigtail Colour | uaEFI Description | Description | Subaru Connector | Subaru Pin | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| A1  | white  | etb (DC1-) | **Electronic Throttle Body (-)** | | | |
| A2  | white  | etb (DC2-) | | | | |
| A3  | black  | gnd (Power Ground) | | | | |
| A4  | black  | gnd (Power Ground) | | | | |
| A5  | blue   | etb (DC1+) | **Electronic Throttle Body (+)** | | | |
| A6  | blue   | etb (DC2+) | | | | |
| A7  | red    | Ignition SW / Batter Voltage Analog Input | | | | |
| A8  | red    | +12V From Main Relay | | | | |
|     |        | | | | | |
| B1  | grey   | Injector Output 6 | | | | |
| B2  | yellow | Injector Output 5 | | | | |
| B3  | orange/brown | Injector Output 4 | **Injector #4** | | | |
| B4  | blue   | Injector Output 3 | **Injector #3** | | | |
| B5  | white  | Injector Output 2 | **Injector #2** | | | |
| B6  | green  | Injector Output 1 | **Injector #1** | | | |
| B7  | orange | VVT1 or Low Side Out 1 (flyback D2) | | | | |
| B8  | red    | **Fan Relay** Weak Low Side Out 2 (no flyback) | *Fan Relay* | | | |
| B9  | grey   | **Main Relay** Weak Low Side Out 1 (no flyback) | *Main Relay* | | | |
| B10 | grey   | Coil 6 (5v) | | | | |
| B11 | orange | Coil 4 | | | | |
| B12 | blue   | Coil 3 | | | | |
| B13 | yellow | Coil 5 | | | | |
| B14 | white  | Coil 2 | | | | |
| B15 | green  | Coil 1 (5v) | | | | |
| B16 | white  | **Fuel Pump Relay** Low Side Out 4 (flyback D5) | | | | |
| B17 | yellow | Low Side out 3 (flyback D4) | | | | |
| B18 | grey   | VVT2 Low Side out 2 (flyback D3) | | | | |


