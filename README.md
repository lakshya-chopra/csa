# csa

## Topics:

### Digital Electronics:
  - Boolean Algebra
  - K maps
  - Combinational Circuits
  - Sequential circuits
  - Flip flops & latches
  - State diagrams, state tables, excitation tables, characteristic tables
  - Designing a sequential circuit.
.... **keep adding**
  
**for questions asking to design a sequential circuit using the given state table**:
  
  - **Read Morris Mano's Computer System Arch. Chap 1 Page 33-37.**

  - Draw a table with columns: Present states, inputs given, next state, Flip flop inputs
  - Note that the number of FF’s = the number of states (considering each FF gives one output).
  - This means, first an excitation table for the present state and then for the next states (where inputs are the ff inputs)
  - Find the boolean expression for FF inputs using K-maps.
  - [Practice Problem](https://www.youtube.com/watch?v=t875Z-VCasQ)
    
  - ### **If checkboard like Pattern in the K-map** : the net simplified expression is just the xor of all the variables involved.

**Latches v/s Flip Flops**:
  - Flip flops are made of two latches connected with each other with one being the master and another, the slave, each having opposite polarity clocks, which makes them edge triggered. While this is not the case with Latches, hence, they are level triggered.
  - [a really good source](https://electronics.stackexchange.com/a/269984)

**Understand the problem T FF solves which JK flip flop doesn't**

**Why does D FF lead to delay?**  

**Why should the clock frequency be higher than the frequency of propagation in the gates to avoid race condition?**

**Realize circuits using universal gates only (eg: implementing Half adder using only NAND GATE)**

### Questions like this: where you have to compute a K-Map and then implement the expression using only certain gates (like 2 NORs, NAND and OR, NAND & AND)
   - [example](https://www.youtube.com/watch?v=8I9WoD4A9R0&list=PLI0y8_sKQPD991sipHcqWNOJ0nmCnqPSw&index=86)
   - [another](https://www.youtube.com/watch?v=SA1V9k3vHvg&list=PLI0y8_sKQPD991sipHcqWNOJ0nmCnqPSw&index=81)

### Logic behind the operation/truth table of encoders and decoders.

### 5 to 32 decoder, using 3-8 decoders only. [helpful](https://www.youtube.com/watch?v=Qcnmb7XuA8Y)

### ADRESSING MODES:
  - Immediate addressing : the value of the operand is specified directly in the instruction (no need to access memory).
  - Implied addressing : When the operand value isn't clearly stated but it is implied, for eg: ADD R1,R2 => Here, it is implied that the contents of R2 need to be added to R1.
  - Direct addressing : stating the memory address of the operand. [This address goes to the AR, which has **address access** to the memory, and then the operand at that address is placed on the common bus, where is loaded into the specified register]
  - Indirect addressing
  - Base Register Relative : Here, the effective address = addr of Base register + the offset (offset can be implemented through the *branch* instruction)
    [Check out](https://www.ibm.com/docs/en/aix/7.1?topic=processor-branch-instructions)
  - PC Relative
  - Indexed Addressing : Effective ADDR = Base addr + value of Index Register.

### If transferring 12 bit data to 16 bit, then add 4 0's in the start of 12 bit data (i.e. move the actual data to LSB)

### DMA: Direct Memory Access allows hardware/external devices to read/write to the main memory, without occupying the CPU for the entire access time, it is implemented using a DMA controller, which can generate memory addresses and initiate read/write cycles. The CPU first initiates the transfer, then the DMA controller supervises and controls the transfer. Eventually, when the transfer is complete, the controller sends an interrupt to the CPU.

![image](https://github.com/lakshya-chopra/csa/assets/77010972/489287b6-04be-45d0-94f3-2c2286a96936)

### Pipeline: Pipelining is a technique in which a sequential process is divided into various sub operations with each sub operation being executed in a dedicated segment of the CPU, concurrently. The result obtained from the computation of each segment is then transferred to the next segment. Thus, it reduces the number of clock cycles and improves efficienCY.
![Img](https://s0.stackpointer.io/wp-content/uploads/2009/02/pipelining.png)
<br>
[nice quora answer](https://www.quora.com/What-is-pipelining/answer/Ryan-Lam-1)

One of the major complications with deep pipelining (eg, 31-stage pipelining used in some of the Intel Pentium 4 processors) is when a conditional branch instruction is being executed – due to the fact that the processor will not be able to determine the location of the next instruction, therefore it has to wait for the branch instruction to finish and the whole pipeline may need to be flushed as a result. If a program has many conditional branch instructions, pipelining could have a negative effect on the overall perfomance. To alleviate this problem, branch prediction can be used, but this too can have a negative effect if the branches are predicted wrongly.

[quoted from](https://stackpointer.io/hardware/how-pipelining-improves-cpu-performance/113/)


    
     
