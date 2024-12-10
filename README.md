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

**FULL ADDER**
![Truth table](https://github.com/user-attachments/assets/abd68121-225a-4a3c-befc-fd482d4b1fa6)

**FULL SUBRACTOR**
![full-subtractor-truth-table](https://github.com/user-attachments/assets/de3e8600-733b-4c14-9857-23d3f4eedb08)

**Procedure**
1. Type the program in quartus software.
2. Compile and run the porgram.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for the input and ouput to generate the timing diagram.
5. For different input ocmbination generate the timing diagram.

**Program:**

Full Adder:
```
//FULL ADDER
module Exp4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire s1,c1,c2;
xor (s1,a,b);
and (c1,a,b);
xor (sum,s1,cin);
and (c2,s1,cin);
or (cout,c2,c1);

endmodule
```
Full Subractor:
```
//FULL SUBRACTOR
module Exp4_2(df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
```
Designer name: Ashqar Ahamed S T

Register number: 24004759

**RTL Schematic**

**FULL ADDER**
![Exp4](https://github.com/user-attachments/assets/dc6f482a-35ee-49b2-9d4d-e58d894daec0)

**FULL SUBRACTOR**
![Exp4_2](https://github.com/user-attachments/assets/4279f93a-a9f5-435b-a285-f7ab893780af)

**Output Timing Waveform**
**FUll ADDER**
![Ex4(2)](https://github.com/user-attachments/assets/a861dab1-1126-4a26-b313-af1f5ae01150)


**FULL SUBRACTOR**
![Exp4_2(2)](https://github.com/user-attachments/assets/47e7fa24-62e1-4c95-86f5-1859a5f511dd)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



