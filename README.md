**NAME:T.SANJAI
REGISTER NUMBER:24900899**

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

![image](https://github.com/user-attachments/assets/2a049914-8ef4-4037-be61-60d31dcef437)


**Procedure**
Type the program in Quartus software.

1.Compile and run the program.

2.Generate the RTL schematic and save the logic diagram.

3.Create nodes for inputs and output to generate the timing diagram.

4.For different input combinations generate the timing diagram.


**Program:**

**FULL ADDER**

module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
wire w1,w2,w3;
assign sum=a^b^c;
assign w1=a&b;
assign w2=a&b;
assign w3=a&b;
assign carry=w1|w2|w3;
endmodule

**FULL SUBTRACTOR**

module fullsub(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
wire w1,w2,w3,w4,w5,w6;
xor g1(diff,a,b,bin);
and g2(w4,w2,b);
and g3(w5,w1,b);
and g4(w6,b,bin);
or g5(borr,w4,w5,w6);
endmodule

**RTL Schematic**

**FULL ADDER**

![image](https://github.com/user-attachments/assets/5d2f43bb-b32f-427b-970a-9f9b46917418)

**FULL SUBTRACTOR**

![image](https://github.com/user-attachments/assets/00f45c4e-55e9-42f6-ba00-8be523aa95e7)



**Output Timing Waveform**

**FULL ADDER**

![image](https://github.com/user-attachments/assets/b70e5598-1e99-4170-895f-39a52e170461)


**FULL SUBTRACTOR**

![image](https://github.com/user-attachments/assets/93f92c96-aeac-4028-a223-2fc3ef3c2dfb)




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



