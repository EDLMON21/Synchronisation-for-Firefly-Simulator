
## Project Overview

### Project Name: Synchronisation-for-Firefly-Simulator
### Team Number: [MON-21]
### Team Members:
- Mohammad Sami
- Shivam Panwar
- Sumanth 
- Yashwanth
- Lokesh (if applicable)

### Problem Statement and Solution:

Synchronization is a key phenomenon in complex systems. So to study it we need a programmable synchronization system with adjustable parameters to study real-time effects.
Classical electronic fireflies (1993 design) lacked programmability and flexibility. Now, Modern advancements in microcontrollers enable digital control & experimentation.

Initial Prototype: We will first design a basic STM32 board with just the microcontroller. This will help us gain hands-on experience with PCB design using the STM32G030X.

Second Iteration: We will integrate IR LEDs, photodiodes, and other components onto the board and fabricate 2-3 units. These will be tested for functionality, synchronization accuracy, and any necessary design refinements.

Final Prototype: After validating the second iteration, we will manufacture 9 boards (to form a 3×3 matrix) for full-scale testing. Any design improvements identified in the previous step will be incorporated into this version.

Throughout this process, software development and implementation will run in parallel, ensuring efficient debugging and integration.
The choice of STM32G030X was recommended by our professor due to its suitability for the application. The IR LED and receiver pair was selected for its strong resistance to ambient light interference, ensuring reliable synchronization.

### The choices of our components

STM32G030K8T6 - STM32G030 series was fixed by the porf. then we chose this model since it was sufficient for our use case and due to ease of soldering and availability.

IR LED and phototransistor pair - SFH 4550  SFH 309 FA. IR was used to avoid interference from visible and photodiode which had the max sensitivity at around 850nm (our ir led wavelength) and had a very small FOV.

Other components like transistor, LDO, micro USB connector were used which are available in WEL.



