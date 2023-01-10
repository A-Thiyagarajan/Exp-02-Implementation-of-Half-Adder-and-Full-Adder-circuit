# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit
# Implementation-of-Half-Adder-and-Full-Adder-circuit
# AIM:
#### Ref number :22008681 A.Thiyagarajan
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

# Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
# Theory
Adders are digital circuits that carry out addition of numbers.

## Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

## Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

# Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
# Program:
## Half adder:
```
module Halfadder(A,B,Sum,Carry);
input A,B;
output Sum,Carry;
xor(Sum,A,B);
and(Carry,A,B);
endmodule
```
## Full adder:
```
module fulladder(A,B,C,Sum,Carry);
input A,B,C;
output Sum,Carry;
assign Sum = ((A^B)^C);
assign Carry = ((A&B)|(B&C)|(C&A));
endmodule
```

# Logic symbol & Truthtable
## Half adder
![half adder symbol and table](https://user-images.githubusercontent.com/118707693/211635229-f50fcf6a-4628-430f-802a-4892a532d3f7.png)
## Full adder
![half adder symbol and table](https://user-images.githubusercontent.com/118707693/211635274-d09a0ff7-2022-411c-a16e-01f582417f3f.png)

# Output:
## Half adder
![half adder diagram](https://user-images.githubusercontent.com/118707693/211629746-8c3c50d8-dac4-41f6-b6f8-e8b41e94100c.png)
## FUll adder
![fulladder](https://user-images.githubusercontent.com/118707693/211629960-06034371-7fa5-4bb1-a639-11a0dec81ffe.png)

# TIMING DIAGRAM
## Half adder
![hatimingdiagram](https://user-images.githubusercontent.com/118707693/211630447-d20a50de-b575-4ed1-b9b8-1b971ff4c27a.png)
## Full adder
![full adder td](https://user-images.githubusercontent.com/118707693/211630536-11bcd900-caa9-47c3-af99-c29aee536c8c.png)

# Result:
Thus the half adder and full adder circuits are designed and the truth tables is verified using quartus software.
