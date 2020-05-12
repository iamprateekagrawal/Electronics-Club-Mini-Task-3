### RL in Hexapod
**Problem Statement:** To integrate 19 sensors of an eighteen DOF Hexapod and recreate the exact orientation of the bot in a computer.

**Constraints:**
1. Minimised price as much as possible.
2. Less wiring entanglement/loose structure, else system may collapse/stop.
3. Data latency to be checked upon.

**Ideation:**
Any arm movement => IMU sensor (detection) => data transfer => microcontroller (data processing)

Process | Factors to look on | Device/Method used | Adantages | Disadvantages
--------|--------------------|--------------------|-----------|--------------
Choosing IMU | Small, cheap, good sensitivity, easy implementation, compatible for faster communication | STMicroelectronics [LSM6DSO32](https://www.mouser.in/datasheet/2/389/lsm6dso32-1815462.pdf) iNEMO Inertial Module | 1) very small and compact - 2.5 x 3 x 0.83 mm <br/> 2) bulk order of 19 imu will totally cost around Rs. 4.5k <br/> 3) I2C, I3C, SPI, MIPI interface types available | Wiring maybe difficult as device is too small
Choosing microcontroller | 
