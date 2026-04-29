# Finals Study Guide

Everything on the [Midterm Study Guide](./midterm-study-guide.md) plus the
following.

## Circuit design

* Transistors
  * N transistors: open at rest
  * P transistors: closed at rest
* Logic gates
  * Not, And, Or, Xor (exclusive or)
  * Universal gates: Nand, Nor
* Combinational circuits
  * Arithmetic circuits
    * Multiplexers
      * Choosing an input
    * Decoders
      * Bit set on a particular encoding
    * Adders
      * Half adders
      * Full adders
      * Carries
* Sequential circuits
  * Memory elements
    * SR latches
      * Asynchronous
      * Unstable
    * D latches
      * Asynchronous
    * D flip-flops
      * Synchronous

## Caches

* Locality
  * Spatial locality
    * Favors large block sizes
  * Temporal locality
    * Favors large amount of blocks
* Four questions
  * Where?
  * How?
  * Which?
  * What happens on write?
* Terms
  * Block offset
  * Set index
  * Tag
  * Valid bit
  * Dirty bit
* Organization
  * Direct mapped
  * Fully associative
  * N-way set associative
* Replacement policies
  * Random
  * Least recently used (LRU)
* Write policies
  * On cache hits
    * Write-through
    * Write-back
      * Dirty bit
  * On cache misses
    * Write-allocate
    * No-write-allocate
  * Typical
    * Write-through + no-write-allocate
    * Write-back + write-allocate

## Pipelining

* Start execution of next instruction before current one has fully completed
* Stages
  * Example: Fetch, Decode, Execute, Memory, Writeback
* Latency
* Throughput
* Hazards
  * Data
  * Control
  * Solutions
    * Stall
    * Bypass networks
    * Prediction
      * Guess but verify and restart if necessary
