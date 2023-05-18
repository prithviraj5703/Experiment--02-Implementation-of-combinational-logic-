# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
 
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.
## Logic Diagram
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.
## Procedure
1.Create a project with required entities.
2.Create a module along with respective file name.
3.Run the respective programs for the given boolean equations.
4.Run the module and get the respective RTL outputs.
5.Create university program(VWF) for getting timing diagram.
6.Give the respective inputs for timing diagram and obtain the results.
## Program:
```python
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: prithviraj
RegisterNumber:  212222100038
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: Deepika.J
RegisterNumber:  212221230016
using NAND:
   module combo1(a,b,c,d,f);
   input a,b,c,d;
   output f;
   wire p,q,r;
   assign p=(~c & b & a);
   assign q=(~d & c & ~a);
   assign r=(c & ~b & a);
   assign f=(~(~p & ~q & ~r));
   endmodule

using NOR:
   module combo2(a,b,c,d,f);
   input a,b,c,d;
   output f;
   wire p,q,r;
   assign p=( c & ~b & a);
   assign q=( d & ~c & a);
   assign r=( c & ~b & a);
   assign f=(~(~( p | q | r)));
   endmodule
```
## RTL realization

## Output:
##using NAND gates:
## RTL
![image](https://github.com/prithviraj5703/Experiment--02-Implementation-of-combinational-logic-/assets/121418418/0cb3e07e-3894-43ab-a5c4-ba69219c66ab)

## Timing Diagram
![image](https://github.com/prithviraj5703/Experiment--02-Implementation-of-combinational-logic-/assets/121418418/efca8ba9-557d-44d3-bad1-f01df26530dc)
##Truth Table:
![image](https://github.com/prithviraj5703/Experiment--02-Implementation-of-combinational-logic-/assets/121418418/775092df-6df6-42bf-ad6f-029b64b5073b)
##USING NOR:
##RTL:
![image](https://github.com/prithviraj5703/Experiment--02-Implementation-of-combinational-logic-/assets/121418418/13ed60ad-053f-41ab-ae0e-1a783a64cad9)
##Timing Diagram:
![image](https://github.com/prithviraj5703/Experiment--02-Implementation-of-combinational-logic-/assets/121418418/c6df0620-8340-4638-999f-aeaab0c93510)
##Truth Table:
![image](https://github.com/prithviraj5703/Experiment--02-Implementation-of-combinational-logic-/assets/121418418/2a6d892e-07fc-4933-81fe-a3ad12a6adb2)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
