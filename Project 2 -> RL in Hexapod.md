### RL in Hexapod
**Problem Statement:** To integrate 19 sensors of an eighteen DOF Hexapod and recreate the exact orientation of the bot in a computer.

**Constraints:**
1. Minimised price as much as possible.
2. Less wiring entanglement/loose structure, else system may collapse/stop.
3. Data latency to be checked upon.

**Steps involved:** Any arm movement => IMU sensor (detection) => data transfer => microcontroller (data processing)

**Choosing IMU:-**
* Factors to look on - Small, cheap, good sensitivity, easy implementation, compatible for faster communication
* Device used - STMicroelectronics LSM6DSO32 iNEMO Inertial Module (Need [datatsheet](https://www.mouser.in/datasheet/2/389/lsm6dso32-1815462.pdf)?) 
* Advantages - 
     1) very small and compact - 2.5 x 3 x 0.83 mm <br/> 
     2) bulk order of 19 imu will totally cost around Rs. 4.5k max (can be considered relatively cheap) <br/> 
     3) I2C, I3C, SPI, MIPI interface types available which are fast.
* Disadvantages - Wiring maybe difficult as device is too small

**Connection type between IMU and IC:-**
* Factors to look on - less wiring, more speed, easy implementation, compatibility
* Methods available
    1) I2C - Good speed & complexity, two way wiring, easy for configuration, multipple sensors (Theritically 127 per channel, but actually much lower than this ([Refer here](https://www.bluedot.space/tutorials/how-many-devices-can-you-connect-on-i2c-bus/) for details) - we take 2-3 can be connected per I2C channel.
    2) SPI - Great speed, four way wiring required, difficult configuration, multiple sensors allowed (Theoriticaly as many as we want, but gradually makes the system complex)
    3) Other sensor bus features like IEEE1451.2 TII, IEEE1451.3 IM2 or wireless sensor networks can also be used but they have their own disadvantages like complexity and speed. (Greater details and comparison between all can be found [here](https://www.mdpi.com/1424-8220/2/7/244/pdf))
* Hence, we choose I2C as a good communication method (features listed above)
* Disadvantage:
    1) There's still double wiring involved which increases complexity
    2) I2C needs each slave(IMU) to have different addresses.

**Choosing microcontroller:-**
* Factors to look on - should be compatible with I2C bus, should allow multiple I2C channels for integrating the IMUs, set clock frequency to see to data latency, fair size, good processing speed.
* Device used - TCA9548A (Need [datasheet](https://pdf1.alldatasheet.com/datasheet-pdf/view/879496/TI1/TCA9548A.html) ?)
* Advantages/Features:
    1) We have eight channels and per channel we can connect 2-3 IMUs acting as slaves (all reasons listed above)
    2) Low Standby Current
    3) Other common ones included in datasheet with more clarity and details.
* Disadvantages - There's slight complexity still involved due to multiple channels and their integration.

**Final structure and process:**
* LSM6DSO32 for IMU, TCA9548A for the microcontroller, I2C bus connection between them is ideated (reasons given above)
* The microcontroller initiates communication and collects real-time data from each sensor everytime via I2C bus connections and then sends them to the computer which displays the orientation and initiates any changes in motor configurations according to RL.
