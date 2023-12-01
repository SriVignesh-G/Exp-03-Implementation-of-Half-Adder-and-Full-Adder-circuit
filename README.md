# Name: Sri Vignesh G
# Reference Number: 23012556

# Experiment-3: Implementation of Half Adder and Full Adder circuit
## AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
## Theory
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
 

## Procedure

Connect the supply (+5V) to the circuit

Switch ON the main switch

If the output is 1, then the led glows.

## Program:

### Half Adder:
```
﻿module halfadder (A, B, sum, carry);
input A, B;
output sum, carry;
xor (sum, A, B);
and (carry,A,B);
endmodule
```
### Full Adder:
```
module fulladder(A,B,C,sum,carry);
input A,B,C;
output sum,carry;
assign sum = ((A^B)^C)
assign carry = ((A&b)|(A&C)|(B&C));
endmodule
```

## RTL realization
### Half Adder:
![ex3 hfld](https://github.com/SriVignesh-G/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147576510/c91bd5fd-7d18-4059-a3cc-a0df43391ed4)



### Full Adder
![ex3 ffld](https://github.com/SriVignesh-G/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147576510/a0864c87-041f-4010-9f19-ec1c32f10e31)

## Output:
### TRUTH TABLE 
#### Half Adder:
![tt 3](https://github.com/SriVignesh-G/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147576510/12ebab4c-963b-44db-a84a-1cd036f6ae7b)



#### Full Adder:
![e3 ff](https://github.com/SriVignesh-G/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147576510/7ba27f60-6e29-4ed9-9aef-369c1f732f60)


### TIMING DIAGRAM

#### Half Adder:
![e3 tm hf](https://github.com/SriVignesh-G/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147576510/7d103398-9d7a-48f9-9f45-cbb3a0e0c0fb)



#### Full Adder:
![e3 ff tm](https://github.com/SriVignesh-G/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147576510/898fdac1-85be-4cd4-a63d-a513c184857c)

### Result:
Thus a Half Adder and Full Adder is designed and its truthtables are verified in Quartus using Verilog programming.
