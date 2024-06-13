Assume we have a simple instruction set with the following stages:

1. **Fetch (F)**: Fetch the instruction from memory.
2. **Decode (D)**: Decode the instruction and read registers.
3. **Execute (E)**: Execute the operation or calculate an address.
4. **Memory (M)**: Access memory if needed.
5. **Write-back (W)**: Write the result back to the register.

Let's assume each stage takes 1 clock cycle.

#### Non-Pipelined System

In a non-pipelined system, each instruction must complete all stages before the next instruction starts. For 3 instructions (I1, I2, I3), the execution timeline would look like this:

| Cycle | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   | 10  | 11  | 12  | 13  | 14  | 15  |
| ----- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| I1    | F   | D   | E   | M   | W   |     |     |     |     |     |     |     |     |     |     |
| I2    |     |     |     |     |     | F   | D   | E   | M   | W   |     |     |     |     |     |
| I3    |     |     |     |     |     |     |     |     |     |     | F   | D   | E   | M   | W   |

In this scenario, it takes 15 cycles to complete 3 instructions.

#### Pipelined System

In a pipelined system, multiple instructions can be processed simultaneously by different stages. For 3 instructions (I1, I2, I3), the execution timeline would look like this:

|Cycle|1|2|3|4|5|6|7|
|---|---|---|---|---|---|---|---|
|I1|F|D|E|M|W|||
|I2||F|D|E|M|W||
|I3|||F|D|E|M|W|

In this scenario, it takes 7 cycles to complete 3 instructions.

### Calculating Speedup

The speedup can be calculated using the formula:

$$\text{Speedup} = \frac{\text{Execution Time (Non-Pipelined)}}{\text{Execution Time (Pipelined)}}$$​

For our example:

- **Non-Pipelined Execution Time** = 15 cycles
- **Pipelined Execution Time** = 7 cycles

$$\text{Speedup} = \frac{15}{7} \approx 2.14$$

So, the pipelined system is approximately 2.14 times faster than the non-pipelined system for this example.

### General Speedup Analysis

For a more general analysis, if we have $n$ instructions and each stage takes $T$ clock cycles, the execution time for a non-pipelined system is:

$\text{Execution Time (Non-Pipelined)} = n \times k \times T$

Where $k$ is the number of stages.

For a pipelined system, the execution time is:

$\text{Execution Time (Pipelined)} = (n + k - 1) \times T$

The speedup is then:

$$\text{Speedup} = \frac{n \times k \times T}{(n + k - 1) \times T} = \frac{n \times k}{n + k - 1}$$

For large $n$, the speedup approaches $k$, the number of pipeline stages, indicating that ideally, a pipeline can make the system $k$ times faster, assuming no pipeline hazards and perfect conditions.

In reality, the speedup is often less than $k$ due to pipeline stalls, hazards, and other inefficiencies. However, this theoretical analysis gives a good understanding of the potential benefits of pipelining.