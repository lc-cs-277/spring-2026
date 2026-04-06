# Lab #6: Simply Implementation

In this assignment, you are to build a processor implementing the Simply ISA.

## Tool

We will continue using Helmut Neeman's [simple digital circuit
simulator](https://github.com/hneemann/digital).

## Hints

* For this design we will split memory into two distinct items, (1) Components >
  Memory > ROM for instruction fetches and (2) Components > Memory > RAM > RAM,
  separated Ports for data accesses.
* Store the program you developed in lab 4 (square.out) at the top of your ROM.
* Break down the design into the following phases:
  * Instruction fetch
  * Instruction decode
  * Register fetch
  * Execution (ADD or nothing)
  * Memory access
  * Register writeback

## How do I know it works?

You should be able to single step through the execution of your program (using
the Clock Input component, Component > IO > Clock Input) until the HLT
instruction, at which point the third location of your RAM should contain the
value computed by your program.

## What to hand in

Hand in SIMPLY.dig. Don’t forget to add your name somewhere as text decorations
(Components > Misc. > Decoration > Text).
