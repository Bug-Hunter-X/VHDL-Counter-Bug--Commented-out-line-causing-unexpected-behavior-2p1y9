# VHDL Counter Bug: Commented-out Line Causing Unexpected Behavior

This repository demonstrates a subtle bug in a VHDL counter.  The bug is triggered by a commented-out line of code that unexpectedly affects the execution flow of the subsequent line.  This highlights a potential issue with VHDL's sensitivity list and process execution.

## Bug Description

A simple counter is implemented using a process sensitive to clock and reset signals.  A commented-out line within the process unexpectedly prevents the next line of code from being executed, causing the counter to stop incrementing correctly.

## Bug Reproduction
1. Synthesize the provided VHDL code (`bug.vhdl`).
2. Simulate the design.
3. Observe that the counter stops incrementing after reaching a certain value, even though the code seems to have no obvious errors.

## Bug Solution
The solution involves removing the commented-out line, which will resolve the issue. Removing the comment allows the next line to be executed as expected. This is explained in `bugSolution.vhdl`

## Lessons Learned
This bug highlights the importance of:
* Carefully reviewing even seemingly innocuous commented-out code, as it can affect code execution in unexpected ways.  
* Understanding the sensitivity list in VHDL processes. A more robust approach may use a conditional assignment or separate process to handle more complex scenarios.