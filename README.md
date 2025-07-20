# STM32F411 Nucleo SPI Polling Mode

![STM32F411](https://img.shields.io/badge/STM32F411-Nucleo-blue) 
![SPI](https://img.shields.io/badge/SPI-Polling_Mode-green)

Basic SPI communication in polling mode using STM32F411 Nucleo.

## Features
- **SPI Master Mode** (SPI1)
- **8MHz Clock** (32MHz/4 prescaler)
- **Full-Duplex** communication
- **10-byte Transfer** demonstration
- **Polling Mode** implementation

## Hardware Setup
| Signal | Nucleo Pin | Connection |
|--------|------------|------------|
| MOSI   | PA7 (D11)  | → Slave MOSI |
| MISO   | PA6 (D12)  | ← Slave MISO |
| SCK    | PA5 (D13)  | → Slave SCK |
| NSS    | PA4 (D10)  | → Slave CS (Software controlled) |

## Technical Details
### SPI Configuration 
```c
Mode: Master (SPI1)
Data Size: 8-bit
Clock: Mode 0 (CPOL=0, CPHA=0)
Prescaler: 8 → 4MHz SPI clock (32MHz/8)
