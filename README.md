# Brendan Bezuko - STM32 Based PCB Design

## Requirements

#### Schematic Design
- The product must use MCU LQFP100 STM32L071V8T6. All appropriate circuitry from design guide will need to be added properly.
- The board will have an HAC-UAN433 based Radio Module. The datasheet for the same is pushed in docs folder.
- The board will have a 7-segment based SMD Display ACDC56-41SURKWA-F01. The corresponding BCD to 7-segment decoder proposed by client is MC14511B but **client is expecting better options for the decoder if available**. Datasheets of both parts are present in docs folder.
- The board will have a 50K OHM 2W [potentiometer](https://www.digikey.ca/en/products/detail/precision-electronics-corporation/RV4NAYSD503A/222810) that will poke out of a hole in the center of the PCB. Please ignore the datasheet of potentiometer in docs folder.
- The board will have an encoder PEC11H-4220F-S0024 that also needs to poke out from same hole as above and hence dimension comparison is needed. Datasheet is pushed to docs folder.
- Use level shifters where necessary as STM32 works on 3.3V logic.
- The 3 buttons (4-pin connector) from the old design need to be connected to PA0 (Pin-23), PC13 (Pin-27) and PE6 (Pin-5) respectively.
- Add 3 additional buttons. The connector style will be same as battery connector WM4200-ND. There will be 3 of these 2-pin connectors for each button with connections being button input and GND on each connector for each button.
- Programing interface (SWD) for the STM32 only, no other option should be given.
- The board will have direct power for 5V peripherals (using 3 x AAA batteries) and only an LDO for 3.3V conversion with adequate current supply.
- There will be only one component present at a time, either encoder or potentiometer. Both won't be mounted at same time.

#### PCB Design
- PCB Desgin should be two sided (2 layers).
- See images for exact dimensions and photo example of previous version for layout kept in docs folder.
- Strict Dimensional requirements to fit existing housing roughly 2" x 4"
