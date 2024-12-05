# Project: LED Control with FreeRTOS on STM32

This project demonstrates how to control multiple LEDs on an STM32 microcontroller using FreeRTOS. The project creates several tasks in FreeRTOS to control the LEDs connected to the STM32 board. Each LED blinks at different time intervals, showcasing how to manage critical sections for safe data access across multiple tasks.

## Hardware Configuration
- **LEDs used:**
  - **Green LED** connected to pin PA0.
  - **Red LED** connected to pin PA2.
  - **Blue LED** connected to pin PA1.
  - **Orange LED** connected to pin PA3.

## Key Components:
1. **GPIO Initialization:**  
   The GPIOs are initialized to control the LEDs. Each LED is controlled by changing the state of the corresponding GPIO pin.

2. **FreeRTOS Tasks:**  
   FreeRTOS tasks are created to control the LEDs with specific time intervals. Each task has its own functionality:
   - The Green LED task with a 200 ms interval.
   - The Red LED task with a 550 ms interval.
   - The Orange LED task with a 50 ms interval.

3. **Critical Section:**  
   The critical section mechanism is used to safely access shared data between tasks. This prevents race conditions, ensuring consistent data access across tasks running concurrently.

4. **Controlling LEDs in Tasks:**  
   Each task is responsible for controlling a specific LED. For example, the Green LED task will turn on the Green LED, wait for a few milliseconds, turn it off, and then continue the task. Each LED is controlled by blinking or toggling at predefined intervals.

5. **Using FreeRTOS:**  
   FreeRTOS is used to manage multitasking on the STM32. Each LED is controlled by a separate task, allowing efficient management of time and resources without interfering with other tasks.

## Operation Steps:
1. **Hardware Setup:**  
   Ensure that the STM32 board is connected to the LEDs on the correct GPIO ports (PA0, PA1, PA2, PA3).

2. **FreeRTOS Configuration:**  
   In this project, FreeRTOS is configured to create tasks that control the LEDs. Each task has a different priority and is responsible for manipulating the LEDs at the specified times.

3. **Execution:**  
   After flashing the code to the STM32 board, the LEDs will start blinking according to the intervals defined in the FreeRTOS tasks.

## Conclusion:
This project demonstrates how to use FreeRTOS on the STM32 to control multiple LEDs with different time intervals. It also illustrates the use of critical sections to ensure safe access to shared data between tasks running in parallel. By using FreeRTOS, we can efficiently manage multitasking on the STM32 and handle more operations simultaneously without conflicts.

https://github.com/user-attachments/assets/e692a6ec-67e9-47fa-b6a1-27dd5458795a
