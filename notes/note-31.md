# Note 31

## Combinatorial circuits

So far our circuits were functional in nature: inputs are fed into combinatorial
circuits whose outputs only depend on the inputs. In particular, these circuits
did not depend on some state and have no cycles (or feedback).

## Sequential circuits

Sequential circuits, on the other hand, have state built with feedback loops. We
need state to hold onto the content of our various registers and memory.

### SR latches

* Built with a feedback loop
* Store one bit of state
* Asynchronous (liable to change state on any changes to its input)
* Foundational (basic block to other designs)
* Low power
* Simplest
* Fastest
* But: Unstable when both inputs change from high to low at the same time

### D latches

* Store one bit of state
* Low power
* Simple
* Fast
* No invalid states
* But: Still asynchronous

### D flip-flops

* Store one bit of state
* Synchronous (latches state during a clock transition)
* Commonly used for registers
