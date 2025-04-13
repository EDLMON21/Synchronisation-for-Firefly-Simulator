
## Project Overview

### Project Name: Synchronisation-for-Firefly-Simulator
### Team Number: MON-21
### Team Members:
- Mohammad Sami
- Shivam Panwar
- Gogineni Venkat Sumanth 
- Juluva Yashwanth
- Lokesh

### Problem Statement and Solution:

Synchronization is a key phenomenon in complex systems. So to study it we need a programmable synchronization system with adjustable parameters to study real-time effects.
Classical electronic fireflies (1993 design) lacked programmability and flexibility. Now, Modern advancements in microcontrollers enable digital control & experimentation.

Initial Prototype: We first designed a basic STM32 board with just the microcontroller. This helped us gain hands-on experience with PCB design using the STM32G030K8T6.

Second Iteration: We integrated IR LEDs, photodiodes, and other components onto the board and fabricate 2-3 units. These was tested for functionality, synchronization accuracy, and any necessary design refinements.

Final Prototype: After validating the second iteration, we manufactured 9 boards (to form a 3×3 matrix) for full-scale testing.

Throughout this process, software development and implementation ran in parallel, ensuring efficient debugging and integration.
The choice of STM32G030X was recommended by our professor due to its suitability for the application. The IR LED and receiver pair was selected for its strong resistance to ambient light interference, ensuring reliable synchronization.

### The choices of our components

STM32G030K8T6 - STM32G030 series was fixed by the porf. Then we chose this model since it was sufficient for our use case and due to ease of soldering and availability.

IR LED and phototransistor pair - SFH 4550  SFH 309 FA. IR was used to avoid interference from visible and photodiode which had the max sensitivity at around 850nm (our ir led wavelength) and had a very small FOV.

Other components like transistor, LDO, micro USB connector were used which were available in WEL.


### Running the Application

1. **Microcontroller:** STM32G030K8T6 or STM32G030K6T6
2. **Integrated Development Environment (IDE):** STM32CubeIDE
3. **Steps for compiling and uploading the code to the device:**
    - Install STM32CubeIDE
    - Download the final.ioc file from STM32G030K8T6 folder in the src folder
    - Load the .ioc file in your IDE
    - Save the file to generate code
    - Replace the code of generated main.c file with the code of main.c file inside STM32G030K8T6 folder in the src folder
    - Click on the build icon to build the code
    - Dump the code in the individual microcontrollers using StLink V2 (or similar)
    - Synchronization process will start as soon as the phototransistors start detecting LED flashes
