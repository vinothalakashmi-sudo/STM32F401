# STM32F401 ADC + DMA + UART (Arduino IDE)

## Objective
Implement a system on STM32 Blackpill where:
1. A 100Hz timer triggers ADC conversion
2. ADC data is transferred using DMA
3. Data is transmitted via UART
4. Output is displayed on Serial Monitor

## Hardware Used
- STM32F401CC Blackpill
- ST-Link V2
- CP2102 USB to UART
- 10kΩ potentiometer

## Software
- Arduino IDE
- STM32 Boards Package (STMicroelectronics)

## Pin Configuration
| Function | Pin |
|--------|----|
| ADC Input | PA0 |
| UART TX | PA3 |
| UART RX | PA2 |

## How It Works
- Timer2 generates interrupts at 100Hz
- Each interrupt triggers ADC read
- DMA behavior is simulated using interrupt-driven buffer
- ADC value is sent via UART

## Output
ADC values (0–4095) are displayed on Arduino Serial Monitor at 115200 baud.

## Notes
- Potentiometer must be powered with 3.3V
- pinMode(PA0, ANALOG) is required
- CP2102 VCC should not be connected

## Author
Vinotha R
