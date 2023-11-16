# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

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
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Samyuktha S
RegisterNumber:  212222240089
*/
```
HALF ADDER:
module exp3 (a,b,sum,carry);
input a,b;
output sum,carry;
assign sum = (a^b);
assign carry = (a&b);
endmodule

FULL ADDER:
module exp3b(a,b,Cin,s,c);
input a,b,Cin;
output s,c;
assign s= (a^b^Cin);
assign c = (a&b)|((a^b)&Cin);
endmodule
```
### Output:
### RTL:
HALF ADDER:
![WhatsApp Image 2023-09-01 at 08 54 34](https://github.com/SamyukthaSreenivasan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475703/a2513833-ef7e-4341-9ce5-9cfc8affac4f)

FULL ADDER:
![image](https://github.com/SamyukthaSreenivasan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475703/baa49550-bd95-42f3-ab2c-0fed4ff5123f)


### TIMING DIAGRAM
HALF ADDER:
![image](https://github.com/SamyukthaSreenivasan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475703/5c7cfdec-d00e-4c04-b897-339c5ab0bcbc)


FUL ADDER:
![image](https://github.com/SamyukthaSreenivasan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475703/eed0a60f-325f-4555-b838-16a1e59917f9)



### TRUTH TABLE 
HALF ADDER:
![image](https://github.com/SamyukthaSreenivasan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475703/e40f17bc-1020-4067-b374-ef453392af34)

FULL ADDER:
![image](https://github.com/SamyukthaSreenivasan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475703/1ecaa9c5-f019-49a0-84ac-faa1982e58fb)

### Result:
Thus the Implementation of Half Adder and Full Adder circuit are studied and the truth table for different logic gates are verified.
