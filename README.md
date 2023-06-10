### Ex. No. : 2 
### Date: 31.3.23 
# Implementation of Combinational logic circuit using Verilog HDL
## Aim:
To implement the following Boolean functions using Verilog HDL and to verify the truth table.
1. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
2. F2=xy’z+x’y’z+w’xy+wx’y+wxy

## Components Required:
1.	Laptop with Quartus software and modelsim software.

## Theory:
Combinational Logic Circuits are memoryless digital logic circuits whose output at any instant in time depends only on the combination of its inputs.
The outputs of Combinational Logic Circuits are only determined by the logical function of their current input state, logic “0” or logic “1”, at any given instant in time.

![image](https://github.com/rvinifa/ex.2/assets/133735746/949815d3-0912-49c7-81c0-eea1c148d48e)

The result is that combinational logic circuits have no feedback, and any changes to the signals being applied to their inputs will immediately have an effect at the output. In other words, in a Combinational Logic Circuit, the output is dependant at all times on the combination of its inputs. Thus, a combinational circuit is memoryless.

## Procedure:
1.	Type the program in Quartus software.
2.	Compile and run the program.
3.	Generate the RTL schematic and save the logic diagram.
4.	Create nodes for inputs and outputs to generate the timing diagram.
5.	For different input combinations, generate the timing diagram.

## Simplification:

![image](https://github.com/PresillaMary/ex.2/assets/129305503/5fb503ec-bf97-4e32-808f-fd5a4c4a9c7b)


![image](https://github.com/PresillaMary/ex.2/assets/129305503/4af6d9d5-f24f-44be-ac61-52bde67aecbb)



## Truth Table:

![image](https://github.com/PresillaMary/ex.2/assets/129305503/a41bf824-cc63-497b-967c-b6ed895737f6)

![image](https://github.com/PresillaMary/ex.2/assets/129305503/3a614441-70e9-412b-8770-110283f3300e)


## Program:

~~~
module exp2(a,b,c,d,f1,f2);
input a,b,c,d;
output f1,f2;
wire adash,bdash,cdash,ddash,x,y,z,p,q,r;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
and(x,bdash,ddash);
and(y,adash,b,d);
and(z,a,b,cdash);
or(f1,x,y,z);
and(p,cdash,d);
and(q,a,c);
and(r,b,c);
or(f2,p,q,r);
endmodule
~~~


## RTL Schematic:

![image](https://github.com/PresillaMary/ex.2/assets/129305503/e6d9dc50-7612-4e92-b3f9-e6cdcbc18079)



## Timing Diagram:

![image](https://github.com/PresillaMary/ex.2/assets/129305503/37f19053-5bcd-4369-8e1a-f1b30d1c09e5)





## Result:

Thus the given Boolean functions are implemented in Verilog HDL and the truth table are verified.



