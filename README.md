# STM32F411 Nucleo SPI Polling Mode

![STM32F411](https://img.shields.io/badge/STM32F411-Nucleo-blue) 
![SPI](https://img.shields.io/badge/SPI-Polling_Mode-green)

<img src="https://github.com/user-attachments/assets/5a72e995-7368-4264-94c2-6a3c24e1e8db" width="500" alt="05414600-B875-4191-95CE-3AF596E54D49">
<img src="https://github.com/user-attachments/assets/e593ba66-1a54-4e63-832c-37b3ac510ae5" width="500" alt="FCCC47DC-F339-4934-BA53-E0A3CFA124E6">

Basic SPI communication in polling mode using STM32F411 Nucleo.

## Features
- **SPI Master Mode** (SPI1)
- **8MHz Clock** (32MHz/4 prescaler)
- **Full-Duplex** communication
- **10-byte Transfer** demonstration


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
