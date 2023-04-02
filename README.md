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

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: 212222240064
RegisterNumber: M.Pranathi
*/
For HALF ADDER:

module halfadder(a,b,s,c);
input a,b;
output s,c;
xor (s,a,b);
and (c,a,b);
endmodule

For FULL ADDER:

module fulladder(a,b,ci,s,co);
input a,b,ci;
output s,co;
wire d,e,f;
xor (d,a,b);
xor (s,d,ci);
and (e,ci,d);
and (f,a,b);
or (co,e,f);
endmodule

### Logic symbol 

![image](https://user-images.githubusercontent.com/118343610/229346909-4f866e82-f416-49ad-a125-d1d1bf758cc2.png)


### Output:
### RTL
1) For HALF ADDER:

![Screenshot (9) (2)](https://user-images.githubusercontent.com/118343610/229345880-90786cb6-8dfe-4da8-a124-12a60e066965.png)

2) For FULL ADDER:

![image](https://user-images.githubusercontent.com/118343610/229345942-7c053a7f-f120-46b8-9bf0-a036ae7aef02.png)

### TIMING DIAGRAM
1) For HALF ADDER:

![Screenshot (8) (2)](https://user-images.githubusercontent.com/118343610/229346177-c8c494a6-0189-4049-b464-cee6a3ae7534.png)

2) For FULL ADDER:

![image](https://user-images.githubusercontent.com/118343610/229346381-03ae253a-c9f4-40b2-afb0-858bac7968c5.png)

### TRUTH TABLE
FOR HALF ADDER:

![image](https://user-images.githubusercontent.com/118343610/229346527-9ac744b3-4cab-40db-8eeb-2df46a45cd3c.png)


FOR FULL ADDER:

![image](https://user-images.githubusercontent.com/118343610/229346455-95726a52-5d1f-4cf7-8440-0efeb8a80425.png)

### Result:
Thus half adder and full adder circuit is successfully designed and verified its truth table
in Quartus using Verilog programming.
