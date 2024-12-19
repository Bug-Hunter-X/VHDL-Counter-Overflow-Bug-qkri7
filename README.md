# VHDL Counter Overflow Bug
This repository demonstrates a common error in VHDL code: integer overflow in a counter.  The provided VHDL code implements a simple counter, but lacks proper handling for when the counter reaches its maximum value.  The solution demonstrates how to safely handle this scenario.

## Bug
The bug lies in the `counter` entity's architecture.  When `internal_count` reaches 15, a subsequent clock edge causes an overflow, wrapping the counter back to 0. This silent overflow can lead to unexpected behavior in larger systems.

## Solution
The solution addresses the overflow issue by introducing a conditional statement to prevent the increment when the counter is at its maximum value.

## How to Run
This code can be simulated using a VHDL simulator such as ModelSim, GHDL, or Icarus Verilog.