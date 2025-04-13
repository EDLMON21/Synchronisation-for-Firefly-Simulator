### Description

## Key Algorithm Components:
1. **Phase-based oscillator:** Each board maintains a phase variable (0.0 to 1.0) that continuously increases over time. When it reaches 1.0, the board flashes its LEDs and resets the phase to 0.
2. **Photodiode detection:** The algorithm continuously samples the four photodiodes and detects when a neighboring board flashes (ADC value < 500).
3. **Phase response curve:** When a flash is detected from a neighbor, the board adjusts its own phase according to:
- If early in cycle (phase < 0.5): Advance the phase slightly
- If late in cycle but not about to flash: Delay slightly
- If very near firing (phase > 0.9): Flash immediately
4. **Small randomization:** To break deadlocks and prevent persistent desynchronization, small random variations are added to the timing.

## Implementation Details:
- The code initializes with a random phase and period to ensure boards start off-sync
- The coupling strength parameter (0.15) controls how strongly boards influence each other
- As boards detect each other's flashes, they gradually shift their timing to match
- The algorithm handles all four edges of each PCB by monitoring all photodiodes

This approach gradually leads to complete synchronization of all 9 PCBs in the grid. The algorithm is robust against individual board variations and should work regardless of the initial configuration.