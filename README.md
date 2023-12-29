# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

#### Figure -01 HALF ADDER 
![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -02 FULL ADDER

![image](https://github.com/Prithivirajan2911/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147020085/58837255-73ed-40d2-a949-8ae2ba3a1fd7)

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
###  Program:

### HALF ADDER
```
module Half_Full(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```

### FULL ADDER
```
module Full_adder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule 
```
## Output:
### RTL realization:
#### Half Adder Circuit: 

![image](https://github.com/Prithivirajan2911/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147020085/d248f80d-83f8-4e4f-b459-95a0917b9e7b)

#### Full Adder Circuit: 

![image](https://github.com/Prithivirajan2911/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147020085/c04e96af-e438-4227-9f27-19fdb5c26a9f)

## TIMING DIAGRAM
#### Half Adder Circuit:

![image](https://github.com/Prithivirajan2911/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147020085/269470a1-4372-4088-b8a3-1bd125320fe5)

#### Full Adder Circuit:

![image](https://github.com/Prithivirajan2911/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147020085/cbc50803-1def-4f1b-a7d9-7b12d9fad1fc)
## TRUTH TABLE:
#### Half Adder:

![image](https://github.com/Prithivirajan2911/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147020085/a02c1253-c565-47ee-9371-b03645ed2531)

#### Full Adder:

![image](https://github.com/Prithivirajan2911/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147020085/44297f4a-3a67-49ab-aa10-d330cff54783)

### Result:
Thus, a half adder and full adder circuit and its truth table in Quartus using Verilog programming is verified.
