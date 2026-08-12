# ***Digital-Logic-Gates-Implementation-using-CMOS-Technology***

Logic gates are the fundamental building blocks of every digital system. Although we usually study those using truth tables and logic symbols, inside an integrated circuit these logic functions are actually implemented using transistors.

In **CMOS (Complementary Metal-Oxide-Semiconductor) technology**, logic gates are built by combining PMOS and NMOS transistors in complementary pull-up and pull-down networks. This architecture provides **very low static power consumption, good noise immunity** and has become the standard technology used in modern digital ICs, processors and VLSI systems.

While studying **CMOS Digital & VLSI Design in my 5th sem**, I wanted to understand how the Boolean expressions that we normally solve on paper are translated into actual transistor connections. Instead of only reading the theory, I recreated each basic CMOS gate in LTspice and verified its operation through transient simulation.

### Quick Comparison of my all-Implemented CMOS Gates 
| Gate |	| Boolean Expression |	| Output becomes High when... |
|--------|--------|-------|
| NOT |	| A` |	| Input is LOW |
| NAND |	| (A.B)` |	| At least one input is LOW |
|NOR|	|(A + B)`|	|Both inputs are LOW|
AND	A.B	Both inputs are HIGH
OR	A + B	Any input is HIGH
XNOR	AB + A`B` Or Y = A  B	Inputs are different
XOR	AB` + A`B Or Y = A  B	Inputs are the same

### Observations
During the initial stage, I recreated **NOT, NAND and NOR gates** using ***Logisim Evolution*** because it provides a simple transistor-level interface similar to classroom circuit diagrams.
However, while combining those gates to build more complex logic (such as AND and OR using CMOS inverters), the simulator did not behave as expected for my transistor-level implementation. So, I switch back to my **LTspice.**

### What I Learned
-	CMOS gates are built using complementary PMOS and NMOS networks. 
-	NAND and NOR form the basis of most CMOS logic design. 
-	AND and OR are obtained by combining NAND/NOR with CMOS inverters. 
-	XOR and XNOR require complementary inputs and more complex transistor networks. 
-	Transient analysis makes it easy to verify logic operation for all input combinations.
  
### What Changed After Building These Gates
Before starting this project, CMOS gates were simply logic symbols and Boolean expressions to me. After building each gate transistor by transistor, I began looking at them differently. Every Boolean expression now directly reminds me of a pull-up and pull-down network rather than just a truth table.

One unexpected learning during this project was the **limitation I encountered in Logisim Evolution.** Although it was useful for understanding individual transistor-based gates, combining those gates into larger CMOS networks didn't always produce the expected behaviour. That experience itself was valuable because it showed me why LTspice is preferred for **transistor-level verification**.

This project wasn't about creating a complex design. It was about slowing down and understanding how digital logic is physically implemented before moving on to larger CMOS circuits and VLSI design.
