[![MCHP](images/microchip.png)](https://www.microchip.com)

# Getting Started with Timer/Counter Type A (TCA) Examples (Microchip Studio)

  This repository contains examples of bare metal source code for Timer/Counter Type A (TCA), as described in the [TB3217-Getting Started with Timer/Counter Type A (TCA)](https://ww1.microchip.com/downloads/en/Appnotes/TB3217-Getting-Started-with-TCA-DS90003217.pdf) document from Microchip. The repository contains an Atmel Studio Solution with multiple projects inside:

* [<strong>Generating a Dual-Slope PWM Signal:</strong>](Generating_a_Dual-slope_PWM_Signal) This use case shows how to generate a dual slope 16-bit PWM signal with 1 kHz frequency and 50% duty cycle on a GPIO pin (for more details, see [<strong>Generating a Dual-Slope PWM Signal</strong>](Generating_a_Dual-slope_PWM_Signal))
* [<strong>Generating Two PWM Signals in Split Mode:</strong>](Generating_Two_PWM_Signals_in_Split_Mode) This use case shows how to initialize the timer in Split mode to generate two single-slope 8-bit PWM signals on two GPIO pins, with independent duty cycle and frequency (for more details, see [<strong>Generating Two PWM Signals in Split Mode</strong>](Generating_Two_PWM_Signals_in_Split_Mode))
* [<strong>Using Periodic Interrupt Mode:</strong>](Using_Periodic_Interrupt_Mode) This use case shows how to initialize the timer in Single mode to work as a counter. The counter overflows every 250 ms and triggers an interrupt which toggles a pin (for more details, see [<strong>Using Periodic Interrupt Mode</strong>](Using_Periodic_Interrupt_Mode))


## Related Documentation
More details and code examples on the ATMEGA4809 can be found at the following links:
- [TB3217-Getting Started with Timer/Counter Type A (TCA)](https://ww1.microchip.com/downloads/en/Appnotes/TB3217-Getting-Started-with-TCA-DS90003217.pdf)
- [ATMEGA4809 Product Page](https://www.microchip.com/wwwproducts/en/ATMEGA4809)
- [ATMEGA4809 Code Examples on GitHub](https://github.com/microchip-pic-avr-examples?q=atmega4809)
- [ATMEGA4809 Project Examples in START](https://start.atmel.com/#examples/ATMEGA4809XplainedPro)


## Software Used
- Microchip Studio 7.0.2542 or newer [(https://www.microchip.com/mplab/microchip-studio)](https://www.microchip.com/mplab/microchip-studio)
- ATmega_DFP 1.6.364 or newer Device Pack


## Hardware Used
- ATMEGA4809 Xplained Pro [(ATMEGA4809-XPRO)](https://www.microchip.com/developmenttools/ProductDetails/ATMEGA4809-XPRO)
