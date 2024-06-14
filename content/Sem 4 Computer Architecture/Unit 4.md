### Multiprocessor Architecture

**Taxonomy of Parallel Architectures**

Parallel architectures are classified based on how memory and processors are organized and interconnected. A common taxonomy is Flynn's Taxonomy, which categorizes parallel architectures into four types:

1. **SISD (Single Instruction, Single Data)**: Traditional sequential computers where a single processor executes a single instruction stream to operate on data stored in a single memory.
2. **SIMD (Single Instruction, Multiple Data)**: Multiple processing elements perform the same operation on multiple data points simultaneously. Example: Vector processors.
3. **MISD (Multiple Instruction, Single Data)**: Multiple processors execute different instructions on the same data stream. This architecture is rare.
4. **MIMD (Multiple Instruction, Multiple Data)**: Multiple autonomous processors execute different instructions on different data streams. This is the most common parallel architecture, including both shared memory and distributed systems.

**Centralized Shared-Memory Architecture**

In a centralized shared-memory architecture, multiple processors share a single physical memory. Key aspects include:

1. **Synchronization**: Mechanisms to coordinate the actions of multiple processors, ensuring that they can access shared data safely and correctly. Common synchronization primitives include locks, semaphores, and barriers.

2. **Memory Consistency**: Ensures that all processors see a consistent view of memory. Memory consistency models, such as Sequential Consistency and Weak Consistency, define the order in which memory operations (reads and writes) appear to execute.

3. **Interconnection Networks**: The hardware that connects processors to the shared memory. Common interconnection topologies include:
   - **Bus**: A single shared communication line. Simple and cost-effective but can become a bottleneck.
   - **Crossbar Switch**: A grid that allows any processor to be connected to any memory module simultaneously. Offers high bandwidth but is expensive.
   - **Multistage Network**: Combines multiple stages of switches to route data between processors and memory modules. Examples include omega networks and butterfly networks.

**Distributed Shared-Memory Architecture**

In a distributed shared-memory (DSM) architecture, each processor has its own local memory, but the entire memory is accessible from any processor through a global address space. This provides the abstraction of shared memory while physically distributing it. Key features include:

- **NUMA (Non-Uniform Memory Access)**: Memory access time depends on the memory location relative to the processor. Local memory accesses are faster than remote ones.
- **Cache Coherence Protocols**: Ensure that copies of a shared memory block in different caches are consistent. Examples include MSI, MESI, and MOESI protocols.

**Cluster Computers**

Cluster computing involves connecting multiple independent computers (nodes) to work together as a single system. Characteristics include:

- **Commodity Hardware**: Uses off-the-shelf components.
- **High-Performance Interconnect**: Uses fast network technologies such as InfiniBand or Gigabit Ethernet.
- **Scalability**: Clusters can be scaled by adding more nodes.
- **Distributed Memory**: Each node has its own memory, but the nodes can communicate over the network.
- **Types of Cluster Computing**: [[Types of Cluster Computing]]

### Non von Neumann Architectures

**Data Flow Computers**

Data flow architectures represent computation in terms of the flow of data. Instead of executing a sequence of instructions, data flow computers execute instructions as soon as their input data becomes available. Key features include:

- **Data Flow Graph**: A graph where nodes represent computations and edges represent data dependencies.
- **Parallelism**: Exploits fine-grained parallelism by allowing multiple instructions to execute simultaneously as soon as their operands are ready.

**Reduction Computer Architectures**

Reduction architectures focus on the evaluation of expressions through recursive decomposition. They use principles from functional programming languages. Characteristics include:

- **Reduction Trees**: Represent expressions as trees where nodes are operations and leaves are operands.
- **Lazy Evaluation**: Delays the computation of expressions until their values are needed.

**Systolic Architectures**

Systolic arrays are a type of parallel processor array where data flows rhythmically through a network of processors. Key characteristics:

- **Regular Structure**: Processors are arranged in a regular grid or array.
- **Local Communication**: Processors communicate only with their immediate neighbors, which simplifies wiring and reduces communication delays.
- **Pipelining**: Each processor performs a small part of the computation, passing intermediate results to the next processor in the array. This achieves high throughput.

These concepts represent fundamental ideas in the design and operation of multiprocessor and non von Neumann computer architectures, enabling efficient parallel computation and specialized processing for various computational tasks.