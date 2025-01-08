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
![image](https://github.com/user-attachments/assets/21bd9226-2022-4e2f-af8f-dc1628146ba8)

**Procedure**

1. Write the code in Quartus software by creating a new project wizard.
2. Run the program to get output.
3. Then open RTL viewer and download that image.
4. Open new file with University program VWF
5. Set end timer and execute, then download the waveform.
   
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: John Wilfred Thomas J W 
RegisterNumber: 24013517
*/
full adder 
```
module EXP_4(sum, cout, a, b, cin);
output sum;
output cout;
input a;
input b;
input cin;
wire sl,cl,c2;
xor (sl,a,b);
and(cl,a,b); 
xor(sum, sl, cin); 
and (c2, sl,cin);
or (cout, c2,cl); endmodule

module EXP_4_2 (df, bo, a, b, bin);
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
**RTL Schematic**
![image](https://github.com/user-attachments/assets/0534671c-9761-4359-ad27-94e55c4729b2)
![image](https://github.com/user-attachments/assets/b2f21bd2-4b31-4dd4-9043-d0c977cae10a)

**Output Timing Waveform**
![image](https://github.com/user-attachments/assets/b9f4001a-41c5-4256-854f-48a88218346a)
![image](https://github.com/user-attachments/assets/241e1396-5966-421f-96b2-f97cc4a7e88a)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



