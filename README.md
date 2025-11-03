# UART Emulation Driver

This Linux kernel module emulates UART (Universal Asynchronous Receiver/Transmitter) communication using kernel timers.  
It simulates UART data transmission (TX) and reception (RX) by periodically sending and receiving bytes from internal buffers and logging the activity to the kernel log.

---

## Features

- Simulated UART transmission and reception with configurable baud rate.
- Uses kernel timers to emulate byte-by-byte UART timing.
- Circular buffers for TX and RX with sample ASCII data.
- Demonstrates basic UART behavior in a Linux kernel module environment.

---

## Requirements

- Linux kernel headers installed for your running kernel version.
- Kernel build tools (`make`, `gcc`, etc).
- Root privileges to load/unload kernel modules.

---

## Building the Module

Run:
```bash
make
```
then to insert the module :
```bash
sudo insmod simple_uart_driver.ko
```
to remove it : 
```bash
sudo rmmod simple_uart_driver.ko
```
