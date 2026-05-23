# Reaction_Timer_Game_RTOS
Reaction Timer Game using STM32 Nucleo-F446RE and FreeRTOS demonstrating multitasking, semaphores, interrupt handling, task scheduling, and UART communication.
# Reaction Timer Game using STM32 and FreeRTOS

## Overview
This project implements a Reaction Timer Game using the STM32 Nucleo-F446RE development board and FreeRTOS. The system measures the user's reaction speed by turning ON the onboard LED after a random delay and calculating the time taken by the user to press the onboard push button.

The project demonstrates important RTOS concepts such as multitasking, semaphores, interrupt handling, task scheduling, and UART communication in an embedded system environment.

---

## Features
- FreeRTOS-based multitasking
- Binary semaphore synchronization
- External interrupt handling using EXTI
- UART communication using USART2
- Real-time reaction time measurement
- Random delay generation
- Onboard LED and push button usage only

---

## Hardware Used
- STM32 Nucleo-F446RE
- USB Cable

No external components are required.

---

## Software Used
- STM32CubeIDE
- STM32CubeMX
- FreeRTOS CMSIS_V2
- Tera Term

---

## RTOS Concepts Demonstrated

### 1. Task Management
Multiple FreeRTOS tasks run concurrently:
- LED Task
- UART Task

### 2. Priority Scheduling
Tasks are executed according to assigned priorities.

### 3. Semaphores
Binary semaphore is used for synchronization between interrupt service routine and task.

### 4. Interrupt Handling
External interrupt is generated when the onboard push button is pressed.

### 5. UART Communication
Reaction time results are displayed on Tera Term using USART2.

---

## Working Principle
1. System starts and waits for a random delay.
2. Onboard LED turns ON.
3. User presses onboard push button quickly.
4. Reaction time is calculated using FreeRTOS tick count.
5. Result is displayed on serial terminal.

---

## Pin Configuration

| Peripheral | Pin |
|---|---|
| LD2 LED | PA5 |
| B1 Button | PC13 |
| USART2 TX | PA2 |
| USART2 RX | PA3 |

---

## UART Settings

| Parameter | Value |
|---|---|
| Baud Rate | 115200 |
| Data Bits | 8 |
| Stop Bits | 1 |
| Parity | None |

---

## Expected Output

```text
Get Ready...

LED ON! Press Button Fast!

Reaction Time: 245 ms
Good Reflex!
