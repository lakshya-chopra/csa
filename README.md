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
  
**for questions asking to design a sequential circuit using the given state table**:
  - Draw a table with columns: Present states, inputs given, next state, Flip flop inputs
  - This means, first an excitation table for the present state and then for the next states (where inputs are the ff inputs)
  - Find the boolean expression for FF inputs using K-maps.
  - [Practice Problem](https://www.youtube.com/watch?v=t875Z-VCasQ)
    
  - ### **If checkboard like Pattern in the K-map** : the expression is just the xor of all the arguments involved.

**Latches v/s Flip Flops**:
  - Flip flops are made of two latches connected with each other with one being the master and another, the slave, each having opposite polarity clocks, which makes them edge triggered. While this is not the case with Latches, hence, they are level triggered.
  - [a really good source](https://electronics.stackexchange.com/a/269984)

**Understand the problem T FF solves which JK flip flop doesn't**

**Why does D FF lead to delay?**  

**Why should the clock frequency be higher than the frequency of propagation in the gates to avoid race condition?**

**Learn to realize circuits using universal gates only (eg: implementing Half adder using only NAND GATE)**

### Questions are asked where you have to compute a K-Map and then implement the expression using only certain gates (like 2 NORs, NAND and OR, NAND & AND)
   - [example](https://www.youtube.com/watch?v=8I9WoD4A9R0&list=PLI0y8_sKQPD991sipHcqWNOJ0nmCnqPSw&index=86)
   - [another](https://www.youtube.com/watch?v=SA1V9k3vHvg&list=PLI0y8_sKQPD991sipHcqWNOJ0nmCnqPSw&index=81)

### Learn the logic behind the truth table of 4 to 2 encoder and a 2 to 4 decoder.

### 5 to 32 decoder, using 3-8 decoders only. [helpful](https://www.youtube.com/watch?v=Qcnmb7XuA8Y)
     
