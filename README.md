# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

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

![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: PRITHIVIRAJAN V
RegisterNumber: 23003859
*/
### HALF ADDER
module halfadder(sum,carry,a,b,c);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule
### FULL ADDER
module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
wire x,p,q,r;
xor(x,b,c);
xor(sum,x,a);
and(p,a,b);
and(q,b,c);
and(r,a,c);
or(carry,p,q,r);
endmodule

### Logic symbol & Truthtable
HALF ADDER:

![image](https://github.com/Prithivirajan2911/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147020085/bdc6716b-f269-4c3d-a900-6b4314304c9e)
FULL ADDER:

![image](https://github.com/Prithivirajan2911/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147020085/13fd80d3-ae04-477c-8bca-2f79d870fa2d)

### RTL realization
Half Adder Circuit: 

![image](https://github.com/Prithivirajan2911/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147020085/8ac0eede-9e45-4586-8394-d09529c789ad)
Full Adder Circuit: 

 ![image](https://github.com/Prithivirajan2911/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147020085/23b33073-c281-4fab-a239-c11ef1727603)
### Output:
### TIMING DIAGRAM
Half Adder Circuit: -
![image](https://github.com/Prithivirajan2911/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147020085/c1f7edcc-4ec7-4e53-9e3a-e16e3fc590ff)
Full Adder Circuit: -
![image](https://github.com/Prithivirajan2911/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147020085/5f469b12-c7b7-4f6d-9fba-428b5d80ffb9)

### Result:
Thus, a half adder and full adder circuit and its truth table in Quartus using Verilog programming is verified.
