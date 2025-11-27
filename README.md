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

**Program**:
FULL ADDER:
```
module exp4(a,b,cin,sum,carry); 
input a,b,cin; 
output sum,carry; 
assign sum=( (a ^ b)^cin); 
assign carry= ( (a & b)| ( cin &(a ^ b ))); 
endmodule
```
FULL SUBRACTOR:
```
module exp4(a,b,bin,difference,borrow); 
input a,b,bin; 
output difference,borrow; 
assign difference= ( (a ^ b)^bin); 
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )))); 
endmodule
```


Developed by: RegisterNumber:25018006


**RTL Schematic**
FULL ADDER:
![WhatsApp Image 2025-11-26 at 7 34 30 PM](https://github.com/user-attachments/assets/032e9e36-3dc9-4bc0-a279-e22b2bef23a1)
FULL SUBRACTOR:
![WhatsApp Image 2025-11-26 at 2 44 12 PM](https://github.com/user-attachments/assets/364017c9-c74e-4a59-9b65-fd767eee35f2)





**Output Timing Waveform**
FULL ADDER:
![WhatsApp Image 2025-11-26 at 7 34 30 PM (2)](https://github.com/user-attachments/assets/d9f1efe9-5b32-40d0-a178-7aa321848701)
FULL SUBRACTOR:
![WhatsApp Image 2025-11-26 at 7 34 30 PM (1)](https://github.com/user-attachments/assets/88b57ceb-5b49-4364-89a9-124a9365e738)




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



