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

<img width="585" height="663" alt="image" src="https://github.com/user-attachments/assets/c2a52c54-8c18-47f1-91d4-944646d3481c" />
<img width="768" height="705" alt="image" src="https://github.com/user-attachments/assets/af4c477e-fc05-4f14-aa9e-cc041b842781" />


**Procedure**
```
**Full Adder:**
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

**Full Subtractor:** 
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.
```

**Program:**

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

```
module de4(A,B,Cin,Sum,Carry);
input A,B,Cin;
output Sum,Carry;
assign Sum=A^B^Cin;
assign Carry=A&B|B&Cin|A&Cin;
endmodule
```
```
module de13(A,B,Cin,Difference,Borrow);
input A,B,Cin;
output Difference,Borrow;
assign Difference=A^B^Cin;
assign Borrow=~A&B|B&Cin|~A&Cin;
endmodule
```
```
Developed by:A.Allahbakash
RegisterNumber:212225240007
```


**RTL Schematic**

<img width="571" height="302" alt="Screenshot 2026-03-12 131243" src="https://github.com/user-attachments/assets/393ea233-1fcf-4914-8147-9c2e57acc5a9" />
<img width="504" height="306" alt="Screenshot 2026-03-12 132612" src="https://github.com/user-attachments/assets/c6a5b6a1-c6b4-4404-8818-a9eca79030f1" />

**Output Timing Waveform**

FULL ADDER:
<img width="1901" height="982" alt="Screenshot 2026-03-12 131523" src="https://github.com/user-attachments/assets/240290e1-b29f-4dfe-b933-3d5451469858" />
FULL SUBTRACTOR:
<img width="1912" height="988" alt="Screenshot 2026-03-12 132752" src="https://github.com/user-attachments/assets/414d13f5-46b5-4928-8742-76aedac3fabc" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



