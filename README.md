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
```vhd1
module adders(a,b,c,sum,carry,sum1,carry1);
input a,b,c;
output sum,carry,sum1,carry1;
xor(sum,a,b);
and(carry,a,b);
assign sum1=((a^b^c));
assign carry1=((a&b)|(b&c)|(a&c));
endmodule
```




/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
```
Developed by:Hariharan.S
RegisterNumber:212222050016
```
*/
Logic symbol & Truthtable

RTL realization

### Output:

### RTL![Screenshot (17)](https://github.com/Hariharan2004S/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/123146156/37cda504-e2c4-4ca3-bb39-d0803fad5559)

### TIMING DIAGRAM![Screenshot (19)](https://github.com/Hariharan2004S/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/123146156/63956184-1541-4303-a9fc-7c147d7936ab)



### TRUTH TABLE
Half adder
![adder](https://github.com/Hariharan2004S/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/123146156/2dde2920-4f05-4684-8db3-62549d89a81f)
Full adder
![fulladder](https://github.com/Hariharan2004S/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/123146156/e52f3932-d527-4b9d-bca1-6520e5845759)


### Result:
