# PLC Multi-Motor Sequencer

A professional-grade PLC automation project developed using **CODESYS 3.5**. This project demonstrates a robust architecture for sequential motor control, utilizing industry-standard practices such as modular programming and Finite State Machines (FSM).



## Features

*   **Modular Architecture:** Separation of concerns between Logic (ST), Coordination (Ladder), and Visualization.
*   **Finite State Machine (FSM):** Reliable state transition management using `CASE` structures in Structured Text.
*   **Custom Function Blocks:** Reusable `FB_Motor` block with internal timing and auto-reset logic.
*   **Integrated HMI:** Real-time monitoring and control interface with Start/Stop functionality and status indicators.
*   **Safety Oriented:** Global Stop command that resets all active processes instantly.

##  Project Structure

The project follows a strict organizational hierarchy:
- `01_DUTs`: Data Unit Types (Enumerations for FSM states).
- `02_FBs`: Reusable logic components (Motor Control Block).
- `03_VISU`: HMI Screens and Visualization Manager.
- `04_Programs`: Main logic sequences (PRG_Sequence).
- `GVLs`: Global Variable List for I/O mapping.

## Logic Workflow

1. **IDLE:** System waits for the `xStart` command.
2. **MOTOR 1:** Activates for 5 seconds, then automatically transitions.
3. **MOTOR 2:** Activates for 5 seconds.
4. **MOTOR 3:** Activates for 5 seconds.
5. **RESET:** After the final stage, the system returns to IDLE or restarts the cycle.



## Technical Stack

*   **Software:** CODESYS V3.5
*   **Languages:** 
    *   **LD (Ladder Diagram):** Used for top-level program calls.
    *   **ST (Structured Text):** Used for core logic and state transitions.
*   **Platform:** CODESYS Control Win V3 (SoftPLC).

## How to Use

1. Clone this repository.
2. Open the `.project` file in CODESYS.
3. Set the communication path to your local **Gateway**.
4. Compile the project (`F11`).
5. Enter **Simulation Mode** and Login.
6. Open the `Main_Screen` visualization to operate the system.

## Author

Jordan Willian Marques Pereira

Contact: jordan.willian.mp@gmail.com