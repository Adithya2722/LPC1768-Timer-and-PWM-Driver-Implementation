# LPC1768 Timer & PWM Driver (Bare-Metal Embedded C)

## Overview
This project demonstrates bare-metal embedded programming on the LPC1768 microcontroller using Embedded C. It focuses on configuring Timer0 for interrupt-based LED control and generating PWM signals using PWM1.

---

## Features
- Timer0 interrupt-based LED toggling
- PWM signal generation using PWM1
- Register-level programming (no HAL or RTOS)
- NVIC interrupt configuration
- Modular driver structure (Timer, PWM, GPIO)

---

## Technologies Used
- Embedded C
- ARM Cortex-M3 Architecture
- LPC1768 Microcontroller

---

## Project Structure

├── src/
│ ├── project_main.c
│ ├── timer.c
│ └── pwm.c
├── include/
│ ├── timer.h
│ ├── pwm.h
│ └── bits.h



## How It Works
- **Timer0** is configured to generate periodic interrupts.
- Inside the interrupt handler, an LED connected to GPIO is toggled.
- **PWM1** is configured to generate a PWM signal on pin P2.0 (PWM1.1).
- Duty cycle and frequency are controlled using match registers (MR0, MR1).


## Key Concepts Covered
- Timer configuration and interrupts
- PWM signal generation
- NVIC interrupt handling
- Register-level peripheral control


## How to Run
1. Open the project in Keil uVision (or your preferred IDE).
2. Compile the code.
3. Flash it to the LPC1768 using Flash Magic or similar tool.
4. Observe:
   - LED blinking via Timer0 interrupt
   - PWM signal on P2.0 using oscilloscope/LED


## Output
- LED toggles periodically
- PWM waveform generated (50% duty cycle by default)


## Future Improvements
- Add ADC-based PWM control
- UART debugging messages
- RTOS-based task scheduling
- Dynamic duty cycle control
