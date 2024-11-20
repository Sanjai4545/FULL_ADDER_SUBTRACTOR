**NAME:T.SANJAI
REGISTER NUMBER:24900899

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
![Screenshot 2024-11-20 135116](https://github.com/user-attachments/assets/ffb663cc-5ecc-4f18-ad64-1ca60e5ef9e5)

**Procedure**
FULL ADDER
A full adder is a digital circuit that adds three one-bit binary numbers to produce a two-bit output. The procedure for a full adder is as follows: 
The first two inputs are A and B, and the third input is an input carry as C-in. 
The output carry is designated as C OUT and the normal output is designated as S. 
A full adder circuit is implemented using two XOR gates, two AND gates, and an OR gate. 
FULL SUBRATCTOR
A full subtractor performs the subtraction of a given binary bit and generates outputs as differences and borrow. The procedure for a full subtractor is as follows: 
To perform subtraction, use the 2's complements to convert the subtraction to addition. 
A full subtractor can be implemented using universal gates, such as NAND or NOR gates. 
A total of 9 NAND/NOR gates are required to implement a full subtractor. 
A full subtractor can be implemented as 2 half subtractors + OR gate. 


Write the detailed procedure here

**Program:**
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
![WhatsApp Image 2024-11-20 at 1 55 05 PM (1)](https://github.com/user-attachments/assets/3dc00936-4f87-46b6-a667-3ced2c01f635)


**Output Timing Waveform**
![WhatsApp Image 2024-11-20 at 1 55 04 PM](https://github.com/user-attachments/assets/d6f4f468-ca17-4cee-9280-3f82d3f48f10)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



