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
![WhatsApp Image 2025-04-23 at 22 03 32_2e3b2d6b](https://github.com/user-attachments/assets/c80377ce-a8d2-4b81-958a-2def6e4a628c)


![WhatsApp Image 2025-04-23 at 22 03 43_770ae00e](https://github.com/user-attachments/assets/d71f991d-b8a7-417d-a50b-e94bcf91ab85)



**Procedure**

Write the detailed procedure here

**Program:**

```
module faexp(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
FULL SUBTRACTOR:
module fsexp(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule


```

 Developed by: RegisterNumber:212224050027


**RTL Schematic**

![WhatsApp Image 2025-04-23 at 21 13 43_8023bc82](https://github.com/user-attachments/assets/5ba9276c-f2c1-4f31-8af5-2b44a8c0b659)

![WhatsApp Image 2025-04-23 at 21 13 44_82e0f676](https://github.com/user-attachments/assets/343c5e5d-0f1d-4b40-ae6c-af841227fe9a)


**Output Timing Waveform**

![WhatsApp Image 2025-04-23 at 21 13 46_9c5f72a8](https://github.com/user-attachments/assets/b372cb3b-d527-4f6b-96d5-a0cb629ebb7f)


![WhatsApp Image 2025-04-23 at 21 14 17_cfbaf849](https://github.com/user-attachments/assets/90554fce-fa50-4818-bbae-8a711b4a26e8)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



