# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**

```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: KISHORE KUMAR B
RegisterNumber:212225240073
```
```
module EXP4FULLSUBTRACTOR(A,B,Cin,Difference,Borrow);
input A,B,Cin;
output Difference,Borrow;
assign Difference=A^B^Cin;
assign Borrow=~A&B|B&Cin|~A&Cin;
endmodule
```
```
module EXP4FULLADDER(A,B,Cin,Sum,Carry);
input A,B,Cin;
output Sum,Carry;
assign Sum=A^B^Cin;
assign Carry=A&B|B&Cin|A&Cin;
endmodule
```



**RTL Schematic**

<img width="1302" height="677" alt="Screenshot 2026-03-12 140444" src="https://github.com/user-attachments/assets/86c9f42f-d5b6-4ecc-9164-ecf69924d5d3" />
<img width="1050" height="559" alt="Screenshot 2026-03-12 140911" src="https://github.com/user-attachments/assets/c3c145ad-0835-4232-8de1-24c81a8789a5" />



**Output Timing Waveform**
<img width="1920" height="1080" alt="Screenshot 2026-03-12 140638" src="https://github.com/user-attachments/assets/f0649824-010a-43f1-870b-c6e314408aa4" />
<img width="1920" height="1080" alt="Screenshot 2026-03-12 141040" src="https://github.com/user-attachments/assets/a819d4e3-8a8d-43c7-a36d-376cb8a05d91" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



