## Overview
### Introduction to Computer Architecture and Performance Measurement

#### Basic Computer Architecture (Revisited)

**Computer Architecture** refers to the design and organization of a computer's core components, including the CPU, memory, and I/O systems. Key concepts include:

- **CPU**: Central Processing Unit, the brain of the computer, executes instructions.
- **Memory Hierarchy**: Includes registers, cache, RAM, and storage.
- **I/O Systems**: Handles input from and output to external devices.
- **Buses**: Communication pathways for data transfer between CPU, memory, and I/O devices.

#### Quantitative Techniques in Computer Design

Quantitative techniques are used to evaluate and improve computer system performance. These techniques involve:

- **Benchmarks**: Standard tests to measure performance (e.g., SPEC, TPC).
- **Performance Metrics**: Throughput, latency, and efficiency.
- **Amdahl’s Law**: Formula to find the maximum improvement possible with a given enhancement.
- **Speedup**: Measure of performance improvement from enhancements.
- **Further Explanation**: [[Performance Metrics]]

#### Measuring and Reporting Performance

Performance measurement involves:

- **Execution Time**: Total time to complete a task.
- **CPI (Cycles Per Instruction)**: Average number of cycles per instruction.
- **MIPS (Million Instructions Per Second)**: Rate of instruction execution.
- **Benchmarks and Profiling Tools**: Use to assess performance of systems and applications.
- **Further Details**: [[Benchmarks and profiling]]

### Pipelining in Computer Architecture

Pipelining is a technique used to improve the throughput of a CPU by executing multiple instructions simultaneously in different stages of completion.

#### Basic Concepts

- **Pipeline Stages**: Typical stages include *Fetch*, *Decode*, *Execute*, *Memory* *Access*, and *Write Back*.
- **Instruction Pipeline**: Execution of multiple instructions overlapped in a pipeline.
- **Arithmetic Pipeline**: Division of arithmetic operations into sub-operations to increase throughput. [[Arithmetic Pipeline|Read more...]]

### Example-
[[Pipelined system vs non Pipelined system]]


#### Hazards in Pipelining

- **Data Hazards**: Occur when instructions depend on the results of previous instructions.
    - **Solutions**: Data forwarding, pipeline stalls.
- **Control Hazards**: Arise from branch instructions that change the flow of execution.
    - **Solutions**: Branch prediction, speculative execution.
- **Structural Hazards**: Occur when hardware resources are insufficient to support all instructions in the pipeline.
    - **Solutions**: Hardware resource duplication, pipeline interlocks.

#### Techniques for Handling Hazards

- **Data Forwarding**: Passing the result of an operation directly to a subsequent operation.
- **Pipeline Stalls (Bubbles)**: Introducing delay to wait for hazard resolution.
- **Branch Prediction**: Guessing the outcome of a branch to reduce control hazards.
- **Speculative Execution**: Executing instructions before the certainty of the branch direction.

### Exception Handling in Pipelining

- **Exceptions**: Events that disrupt the normal flow of execution (e.g., interrupts, faults).
- **Handling Mechanisms**: Techniques to save the state and ensure correct program execution post-exception.

Further details on the above topics here: [[Pipelining Hazards]]

#### Pipeline Optimization Techniques

- **Instruction Reordering**: Rearranging instructions to avoid hazards.
- **Loop Unrolling**: Expanding loops to reduce loop control overhead and increase pipeline efficiency.
- **Out-of-Order Execution**: Executing instructions as resources are available rather than strictly in order.
- **Non Linear Pipelining**: [[Non Linear Pipelining]]

#### Compiler Techniques for Improving Performance

- **Code Scheduling**: Rearranging code to minimize stalls.
- **Inlining**: Replacing a function call with the function code itself.
- **Register Allocation**: Efficient use of CPU registers to minimize memory access.