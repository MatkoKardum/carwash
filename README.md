# Car Wash Control System

## Overview
This project implements a simulated car wash control system using a PIC microcontroller. The system integrates virtual sensors and actuators in Proteus, applying electropneumatic/hydraulic principles inspired by national championships for sequential timing. The firmware, developed in C, controls a car wash sequence with phases for pre-wash, soaping, rinsing, and drying, using GPIO for sensor/actuator control and PWM for pumps/valves. The project includes firmware, simulation files, and configuration for prototyping and testing.

## Directory Structure
- **Code/**: Contains firmware source code and compiled output for the PIC microcontroller.
  - `carwash.fcf`: Flowcode project file defining the car wash sequence logic and/or keypad input (if applicable).
  - `carwash.hex`: Compiled firmware for programming the PIC microcontroller to manage the car wash sequence.
- **Simulation/**: Includes simulation files for Proteus.
  - `carwash.pdsprj`: Proteus project file simulating the car wash system with virtual sensors (proximity, pressure) and actuators (pumps, valves) using electropneumatic/hydraulic principles.

## Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   ```
2. **Code**:
   - Install MPLAB X IDE with XC8 compiler for PIC microcontroller firmware development.
   - Optionally, install Flowcode (version 8 or later) to open `carwash.fcf` for modifying sequence logic or keypad input (if used).
   - Compile the C source code in MPLAB X IDE or Flowcode to generate/update `carwash.hex`.
   - Flash `carwash.hex` to the PIC microcontroller using a programmer (PICkit, MPLAB ICD).
3. **Simulation**:
   - Install Proteus (version 8 or later recommended).
   - Open `carwash.pdsprj` in the `Simulation/` directory to simulate the car wash system.
   - Verify sequential timing for pre-wash, soaping, rinsing, and drying phases, including virtual sensors (for detecting car presence) and actuators (pumps/valves via PWM).

## Requirements
- **Software**:
  - MPLAB X IDE with XC8 compiler (for C firmware development).
  - Flowcode (optional, for editing `carwash.fcf` if used for sequence or keypad logic).
  - Proteus (for running `carwash.pdsprj` simulations).
- **Hardware**:
  - PIC microcontroller (PIC16F877).
  - Virtual sensors and actuators in Proteus (proximity sensors, pressure sensors, pumps, valves).
- **Dependencies**:
  - Ensure MPLAB XC8 libraries for GPIO and PWM control are included in `Code/`.
  - Verify Proteus component models for the PIC microcontroller, keypad (if used), sensors, and actuators are available.

## Usage
1. **Firmware Development**:
   - Modify C source code in MPLAB X IDE or `carwash.fcf` in Flowcode to customize the car wash sequence (timing for pre-wash, soaping, rinsing, drying) or keypad input handling (if applicable).
   - Compile the project to generate or update `carwash.hex`.
   - Flash `carwash.hex` to the PIC microcontroller using a compatible programmer.
2. **Simulation**:
   - Run `carwash.pdsprj` in Proteus to test the car wash sequence, including sensor inputs (car detection) and actuator outputs (pump/valve control via PWM).
   - Verify sequential timing and electropneumatic/hydraulic behavior in the simulation.
3. **Hardware Implementation**:
   - Connect the physical hardware (PIC microcontroller, sensors, actuators, keypad if used) as per the circuit defined in `carwash.pdsprj`.
   - Test the programmed microcontroller with the car wash system for real-world functionality.

## Contributing
- Fork the repository and create a new branch for your feature or bug fix.
- Submit pull requests with clear descriptions of changes.
- Ensure firmware modifications are compatible with MPLAB X IDE or Flowcode, and simulations work in Proteus.

## License
This project is licensed under the MIT License - see the `LICENSE` file for details.

## Contact
For questions or support, open an issue on the repository or contact matej.kardum.contact@gmail.com
