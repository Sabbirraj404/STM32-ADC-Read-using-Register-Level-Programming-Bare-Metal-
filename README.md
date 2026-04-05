# STM32 ADC Read (Bare Metal - ADC1)

This project demonstrates how to read analog data using STM32F4 (STM32F446RE) with register-level programming (no HAL/LL). ADC1 is used to read an analog signal from GPIOB pin.

---

## Features

- Bare-metal (register-level) programming
- ADC1 single channel read
- No HAL or external libraries
- Simple polling method

---

## Working Principle

- Analog signal is applied to ADC input pin
- ADC converts analog voltage → digital value
- 12-bit resolution (0–4095)

---

## Configuration Details

- ADC: ADC1
- Channel: 8 (PB0)
- Resolution: 12-bit
- Conversion Mode: Single conversion
- Trigger: Software trigger

---

## Hardware Connections

- Analog Input → PB0 (ADC1_IN8)
- GND → Common Ground

---

## Code Explanation

### Enable Clock
- GPIOB clock enabled
- ADC1 clock enabled

### GPIO Configuration
- PB0 set to Analog mode

### ADC Setup
- Channel 8 selected
- ADC enabled

### Conversion Process
1. Start conversion
2. Wait for End Of Conversion (EOC)
3. Read ADC value from DR

---

## Output

- ADC value stored in variable:
  ```
  adc_value (0 – 4095)
  ```
- Can be monitored using debugger (Live Expression)

---

## Requirements

- STM32F446RE
- Analog sensor / potentiometer
- ST-Link Debugger
- Keil / STM32CubeIDE

---

## Learning Outcomes

- ADC register configuration
- Analog to digital conversion
- Polling method
- Embedded C (bare-metal)

---

## Future Improvements

- Continuous conversion mode
- Interrupt-based ADC
- DMA-based ADC
- Multi-channel scanning

---

## Author

Md.Samiul Islam Sabbir
