# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure
Write the detailed procedure here 

1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represnt onre for differnce and the other for borrow.

5.End the verilog program using keyword endmodule.

## Program:
~~~
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: DHIVYA SHRI B
RegisterNumber:212221230009
~~~
## Half Subractor:
~~~
module exp3(output B,D, input X,Y);
assign D = (X ^ Y);
assign B = (~X & Y);
endmodule
~~~
## Full Subractor:
~~~
module exp3(X,Y,Z,B,D);
input X,Y,Z;
output B,D;
assign D = (X^Y^Z);
assign B = (~X&(Y^Z)|(Y&Z));
endmodule
~~~
## Output:
## HALF SUBTRACTOR
## Logic Symbol
![image](https://user-images.githubusercontent.com/94505585/196101794-4b002880-9d7f-4fd8-bb29-e65e9888bef8.png)

## Truthtable:
![image](https://user-images.githubusercontent.com/94505585/196101843-dc46f029-f2f0-4d2b-9b3c-bbf2f044816c.png)

## RTL realization
![image](https://user-images.githubusercontent.com/94505585/196101891-2926ea9d-355c-4195-b337-37c4765f38ad.png)

## Timing diagram
![image](https://user-images.githubusercontent.com/94505585/196101933-21fca040-3afe-4eb7-b1d5-6ed020bc254b.png)

## FULL SUBTRACTOR
## Logic Symbol
![image](https://user-images.githubusercontent.com/94505585/196101984-e6347ec9-0c4c-44f3-8c9c-b25317c9fdda.png)

## Truthtable
![image](https://user-images.githubusercontent.com/94505585/196102022-852206b9-23e3-4a08-99d1-15864baf8aac.png)

## RTL realization
![image](https://user-images.githubusercontent.com/94505585/196102052-02f41163-1805-4447-bd17-d9d409d4699a.png)

## Timing diagram
![image](https://user-images.githubusercontent.com/94505585/196102089-b3a8f886-b638-482f-9787-2dd459a6907c.png)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
