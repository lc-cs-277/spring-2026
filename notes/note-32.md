# Note 32

## Sequential circuits

Combinational circuits, by their nature, do not hold state. To build systems
like processors we must have state. For processors, state usually includes items
such as the instruction pointer register, the general purpose registers, and
possibly a condition code register. This state combines with the combinational
circuits necessary to update said state to form a *sequential circuit* (called
this way because its current state depends on the sequence of past states).

Sequential circuits typically change state on a fixed cadence governed by a
clock (e.g., triggered by a rising clock signal).

The content of all memory elements (e.g., registers) defines the current state
of the system. All or a subset of these memory elements are input into some
combinatorial circuit computing the next state of that system. The clock
controls when this new state is latched into the memory elements. Then the cycle
begins anew with that new state.
