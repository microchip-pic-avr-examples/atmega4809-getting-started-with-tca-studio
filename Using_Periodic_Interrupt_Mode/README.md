[![MCHP](./../images/microchip.png)](https://www.microchip.com)

# Using Periodic Interrupt Mode

This use case shows how to initialize the Timer/Counter Type A (TCA) in Single mode to work as a counter. The counter overflows every 250 ms and triggers an interrupt, which toggles a pin.

## Related Documentation
More details and code examples on the ATMEGA4809 can be found at the following links:
- [TB3217-Getting Started with Timer/Counter Type A (TCA)](https://ww1.microchip.com/downloads/en/Appnotes/TB3217-Getting-Started-with-TCA-DS90003217.pdf)
- [ATMEGA4809 Product Page](https://www.microchip.com/wwwproducts/en/ATMEGA4809)
- [ATMEGA4809 Code Examples on GitHub](https://github.com/microchip-pic-avr-examples?q=atmega4809)
- [ATMEGA4809 Project Examples in START](https://start.atmel.com/#examples/ATMEGA4809XplainedPro)


## Software Used
- Microchip Studio 7.0.2397 or newer [(microchip.com/mplab/microchip-studio)](microchip.com/mplab/microchip-studio)
- ATmega_DFP 1.6.364 or newer Device Pack


## Hardware Used
- ATMEGA4809 Xplained Pro [(ATMEGA4809-XPRO)](https://www.microchip.com/developmenttools/ProductDetails/ATMEGA4809-XPRO)

## Setup
The ATMEGA4809 Xplained Pro Development Board is used as test platform.

<br><img src="../images/atmega4809_xplainedpro.jpg" height="300">

The following configurations must be made for this project:

<Configurations>

System clock is 3.33 MHz.

Global Interrupts Enabled

TCA0:
- Clock Selection: System clock/256
- Timer Mode: 16-Bit (Normal)
- Timer Overflows Every 250 ms
- Enable Overflow Interrupt


| Pin |  Configuration    |
| :-: | :---------------: |
| PA0 |   Digital output  |

 ## Operation
 1. Connect the board to the PC.

 2. Open the atmega4809-getting-started-with-tca-studio.atsln solution in Microchip Studio.

 3. Set the **Using_Periodic_Interrupt_Mode** project as Start-Up project. Right click on the project in the **Solution Explorer** tab and click **Set as StartUp Project**.

<br><img src="../images/Start_Up_Project.PNG" height="500">

 4. Build the **Using_Periodic_Interrupt_Mode** project: Right click on the **atmega4809-getting-started-with-tca-studio** solution and select **Build Solution**.

<br><img src="../images/Build_Solution.PNG"  height="500">

 5. Select the **ATMEGA4809 Xplained Pro** in the Connected Hardware Tool section of the project settings:
   - Right click on the project and click **Properties**
   - Click on the **Tool** tab
   - Select the **ATMEGA4809 Xplained Pro** (click on the **SN**) in the **Selected debugger/programmer** section, and save (CTRL + S):

<br><img src="../images/Select_Tool.PNG" height="500">

 6. Program the project to the board: Click on the **Debug** tab and click **Start Without Debugging**.

<br><img src="../images/Start_Without_Debugging.PNG" height="400">

## Demo

The digital value of the PA0 pin toggled by the TCA0 overflow interrupt can be seen in the following image.

<br><img src="images/Demo.PNG" width="700">

The value of the pin changes every 250 ms.

## Summary

This code example shows how to initialize the TCA as a counter to trigger an overflow interrupt every 250 ms, toggling a GPIO in the Interrupt Service Routine.
