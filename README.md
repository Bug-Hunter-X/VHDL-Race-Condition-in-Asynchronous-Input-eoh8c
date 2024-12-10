# VHDL Race Condition Example

This repository demonstrates a subtle race condition that can occur in VHDL when dealing with asynchronous inputs.

## Description

The `bug.vhdl` file contains a simple VHDL entity that registers an 8-bit input.  However, if the `data_in` signal changes very close to the rising edge of the clock, a race condition can prevent the latest value from being captured.

## Solution

The `bugSolution.vhdl` file shows a possible solution using a synchronous input register and a flip-flop to ensure that the input is properly sampled.  This method avoids the race condition by synchronizing the input to the clock domain.