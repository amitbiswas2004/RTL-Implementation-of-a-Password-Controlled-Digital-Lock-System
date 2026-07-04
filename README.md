# RTL Design and Functional Verification of a Password-Based Digital Locker Controller

## Project Overview

This project implements a password-based digital locker controller using Verilog HDL and a Finite State Machine (FSM). The design authenticates a predefined binary password sequence and controls the lock state based on valid or invalid user inputs. Developed using a synchronous RTL design methodology, the controller is verified through functional simulation in Xilinx Vivado.

---

## Background

Password-based access controllers are widely used in embedded and digital security systems to provide controlled authentication. FSM-based architectures are commonly adopted for such applications due to their deterministic behavior, straightforward implementation, and efficient hardware realization. This project demonstrates the design and verification of an FSM-based digital controller following standard RTL design practices.

---

## Design Objectives

- Design an FSM-based password authentication controller.
- Implement synthesizable RTL in Verilog HDL.
- Verify functional correctness using simulation.
- Validate state transitions under normal and erroneous operating conditions.

---

## Design Specifications

| Parameter | Specification |
|------------|---------------|
| Design Style | RTL |
| HDL | Verilog HDL |
| FSM Type | Moore FSM |
| Password | 1010 |
| Reset | Synchronous |
| Development Tool | Xilinx Vivado |
| Verification | Verilog Testbench |

---

## Repository Structure

```
Digital-Locker-FSM/
│
├── rtl/
├── tb/
├── simulation/
├── docs/
├── images/
└── README.md
```

---

## Design Methodology

The controller is implemented using a Moore Finite State Machine consisting of dedicated states representing each stage of password authentication. Sequential logic stores the present state, while combinational logic determines the next state and output signals. Invalid password entries transition the controller to an error state, whereas successful authentication activates the unlock state.
<img width="989" height="505" alt="image" src="https://github.com/user-attachments/assets/c9a501a1-2441-4927-bc91-28d6d93cf849" />

---

## RTL Implementation

The RTL design consists of:

- State Register
- Next-State Logic
- Output Logic
- Error State Handling
- Reset Logic

The implementation follows synthesizable Verilog coding practices with clearly separated sequential and combinational logic.
<img width="1503" height="679" alt="image" src="https://github.com/user-attachments/assets/b13bce2b-18a3-477c-b5a1-bc4c4bc14be3" />

---

## Functional Verification

Functional verification is performed using a dedicated Verilog testbench. The following scenarios are validated:

- Correct password entry
- Reset operation
- Multiple authentication attempts
- Error state transition

Simulation waveforms are included in the **simulation/** directory.

---

## Vivado Implementation

The project is developed and simulated using **Xilinx Vivado**.

The repository includes:

- RTL Source
- Testbench
- RTL Schematic
- Simulation Waveforms

---

## Results

Simulation confirms correct FSM operation under both valid and invalid input conditions. The controller successfully performs password authentication while maintaining deterministic state transitions and expected lock/unlock behavior.

---

## Future Enhancements

- Configurable password storage
- Keypad interface
- Automatic lockout after repeated failures
- Password update functionality
- FPGA board implementation
- LCD/Seven-segment display interface

---

## Tools

- Verilog HDL
- Xilinx Vivado
- Vivado Simulator

---

## Author

**Amit Biswas**

RTL Design • Digital Design • FPGA Development • VLSI
