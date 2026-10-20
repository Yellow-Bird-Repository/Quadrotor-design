# Bill of Quantities — Crazyflie 2.0 (real hardware)

| Item              | Spec                                                           |   Qty | Linked Parameter                                   |
|:------------------|:---------------------------------------------------------------|------:|:---------------------------------------------------|
| Frame / PCB       | Bitcraze Crazyflie 2.0 main PCB, 92 mm motor-to-motor diagonal |     1 | L = 0.046 m (arm length), m (mass)                 |
| Coreless DC Motor | 7 mm coreless brushed DC motor                                 |     4 | m, T_max (thrust capability)                       |
| Propeller         | 45 mm diameter, 2-blade plastic                                |     4 | T_max                                              |
| Main Flight MCU   | STM32F405 (Cortex-M4, 168 MHz, 192 kB SRAM, 1 MB flash)        |     1 | Executes the feedback law u = u0 - K(x-x0)         |
| Radio/Power MCU   | nRF51822 (Cortex-M0, 32 MHz)                                   |     1 | Command link (transmits u(t) / receives reference) |
| IMU               | MPU-9250 (3-axis gyro + 3-axis accel + 3-axis magnetometer)    |     1 | State feedback: phi, phi_dot measurement           |
| Barometer         | LPS25H high-precision pressure sensor                          |     1 | Altitude z measurement (assists state estimate)    |
| Battery           | LiPo, 3.7 V 1S, ~240 mAh, 7 min flight time                    |     1 | m (mass contribution)                              |
| Radio Link        | Crazyradio PA, 2.4 GHz, >1 km line-of-sight range              |     1 | Ground-station command channel for u(t)            |