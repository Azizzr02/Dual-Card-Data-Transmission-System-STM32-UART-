# Dual-Card-Data-Transmission-System-STM32-UART-
Real-time embedded communication system featuring two STM32 boards with interrupt-driven architecture.
A robust communication system between two STM32 boards using **HAL libraries** and **STM32CubeMX** configuration, demonstrating interrupt-driven UART communication and ADC conversion.

## 📋 Overview
This project implements a dual-microcontroller system where:
- **Transmitter (TX) Board** reads analog values and transmits via UART
- **Receiver (RX) Board** processes incoming data and mirrors LED states

**Key Features**:
- Full configuration through STM32CubeMX (.ioc files included)
- Hardware Abstraction Layer (HAL) driver implementation
- Interrupt-driven architecture for efficient resource usage

## 🛠️ Hardware Setup
### Components
| Component          | TX Board | RX Board |
|--------------------|----------|----------|
| STM32F4xx          | ✓        | ✓        |
| Potentiometer      | ✓        | -        |
| Push Button        | ✓        | -        |
| LEDs (R, G, B, O)  | ✓        | ✓        |
| USB-UART Converter | ✓        | ✓        |

### Connections
```plaintext
TX Board UART2   -> RX Board UART2
PA2 (TX)         -> PA3 (RX)
PA3 (RX)         -> PA2 (TX)
GND              -> GND
