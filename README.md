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
|   ---  | ---        | --- | --- | --- | --- | --- |
| B1  | grey   | Injector Output 6 | | | | |
| B2  | yellow | Injector Output 5 | | | | |
| B3  | orange/brown | Injector Output 4 | **Injector #4** | | | |
| B4  | blue   | Injector Output 3 | **Injector #3** | | | |
| B5  | white  | Injector Output 2 | **Injector #2** | | | |
| B6  | green  | Injector Output 1 | **Injector #1** | | | |
| B7  | orange | VVT1 or Low Side Out 1 (flyback D2) | | | | Variable Valve Timing ??? |
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
|   ---  | ---        | --- | --- | --- | --- | --- |
| C1  | red    | Sensor +5v | | | | |
| C2  | red    | Sensor +5v | | | | |
| C3  | yellow | Aux Analog Input 2 (500k Pull Down) | | | | |
| C4  | orange/brown | PPS2 Universal Analog In | | | | PPS2 ??? |
| C5  | green  | Hall Input 1 (4.7k Pull Up) | | | | All Hall Inputs are 12v Tolerant |
| C6  | blue   | Hall Input 2 (4.7k Pull Up) | | | | All Hall Inputs are 12v Tolerant |
| C7  | white  | Hall Input 2 (4.7k Pull Up) [VSS] | | | | All Hall Inputs are 12v Tolerant |
| C8  | black  | Power Ground (VR Shield) | | | | |
| C9  | grey   | Button In 3 (10k Pull Down) | | | | 12v Tolerant |
| C10 | ???    | EGT (+) Input | | | | What is EGT ???|
| C11 | black  | Sensor Ground | | | | |
| C12 | black  | Sensor Ground | | | | |
| C13 | black  | Sensor Ground | | | | |
| C14 | blue   | Universal Analog Input | | | | |
| C15 | grey   | Fuel Pressure (500k Pull Down) [Analog Input 3] | | | | |
| C16 | blue   | VR2 (+) Input | | | | max9924 best for normal 12+ tooth wheels - *VR = Variable Reluctance" for gear tooth sensors* |
| C17 | white  | VR2 (-) Input | | | | max9924 best for normal 12+ tooth wheels |
| C18 | blue   | VR1 (+) Input | | | | discreet for low count wheel |
| C19 | white  | VR1 (-) Input | | | | |
| C20 | ???    | EGT (-) Input | | | | |
|   ---  | ---        | --- | --- | --- | --- | --- |
| D1  | orange | Aux Analog Input 1 (500k Pull Down) | | | | |
| D2  | yellow | Button In 1 (10k Pull Down) | | | | |
| D3  | red    | Sensor +5v | | | | |
| D4  | red    | Sensor +5v | | | | |
| D5  | orange | Flex Input (10k Pull Up) | | | | |
| D6  | white  | PPS Universal Analog In | | | | PPS (???) What Is ??? |
| D7  | green  | CAN1 Bus High | | | | |
| D8  | blue   | CAN1 Bus Low  | | | | |
| D9  | yellow | MAP Universal Analog Input | | | | |
| D10 | green  | Button In 2 (10k Pull Down) | | | | 12V Tolerant |
| D11 | black  | Sensor Ground | | | | |
| D12 | black  | Sensor Ground | | | | |
| D13 | green  | Universal Analog In | | | | |
| D14 | yellow | Knock Input | | | | Knock (-) goes to Analog Ground |
| D15 | blue   | IAT Input | | | | IAT ??? |
| D16 | grey   | CLT Input | | | | CLT ??? |
| --- | ---    | --- | --- | --- | --- | --- |
| E1  | grey   | WBO Heater (+) Pin #4 | | | | Wide Band Oxygen Sensor |
| E2  | green  | WBO CalR Pin #5 | | | | |
| E3  | white  | WBO Heater (-) Pin #3 | | | | |
| E4  | black  | WBO Vs (Un) Pin #5 | | | | |
| E5  | red    | WBO Ip Pin #1 | | | | |
| E6  | yellow | WBO VS/Ip Pin #2 | | | | |






## Ignition Coils

<img width="796" height="733" alt="image" src="https://github.com/user-attachments/assets/ab75ce66-380f-4ea8-ba19-b9988bf0749a" />

Ok, so this schematic isn't great, because there are many pages that have "Out 1, Out2, ..." but with a little bit of reading of the drawings, it looks we have to add IGBTs for "dumb coils" - The current suspicion is that the coil in this car needs drivers for the coil as they're not a 5v or 12v signal input. Once I figure this out hopefully this will be a useful section.

At minimum if I need the IGBTs, I'll have to remove the bypass 0 ohm resistors on those channels. I will need at most two, since the engine is a wasted spark setup.
