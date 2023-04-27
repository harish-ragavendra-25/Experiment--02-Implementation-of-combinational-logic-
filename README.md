# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Program:
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: HARISH RAGAVENDRA S
RegisterNumber:  212222230045
```
```
module Verilog1(a,b,c,d,w,x,y,z,F1,F2);
input a,b,c,d,w,x,y,z;
output F1,F2;
wire  A1,A2,A3,A4,A5,B1,B2,B3,B4,B5;
assign A1= (~a&(~b)&(~c)&(~d));
assign A2= (a&c&(~d));
assign A3= ((~b)&c&(~d));
assign A4= (~a&b&c&d);
assign A5= (b&(~c)&d);
assign F1= A1|A2|A3|A4|A5;
assign B1= (x&(~y)&z);
assign B2= (~x&(~y)&z);
assign B3= (~w&x&y);
assign B4= (w&(~x)&y);
assign B5= (w&y&z);
assign F2= B1|B2|B3|B4|B5;
endmodule
```
## OUTPUT:

## RTL realization
![Screenshot 2023-04-27 104109](https://user-images.githubusercontent.com/114852180/234767748-dd200d52-52c4-4d52-a2cc-74ec0d9a28c5.png)
![Screenshot 2023-04-27 104136](https://user-images.githubusercontent.com/114852180/234767768-10821aa4-fd08-4b5e-926f-f22b16aedbc9.png)
## Timing Diagram
![Screenshot 2023-04-27 105523](https://user-images.githubusercontent.com/114852180/234768527-c5cb5ffc-7986-45c6-8b12-a1e3c1bd5e62.png)
## TRUTH TABLE:
![Screenshot 2023-04-27 105533](https://user-images.githubusercontent.com/114852180/234768580-dcb05125-d913-42dc-9ecc-40b082236775.png)
## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
