# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

Half adder:
<img width="293" height="172" alt="half adder truth table" src="https://github.com/user-attachments/assets/c6f87081-bd40-49c1-b4d6-455fbb456cdf" />

Half subtractor:
<img width="294" height="172" alt="half subtractor truth table" src="https://github.com/user-attachments/assets/0d2108ec-2ee3-44f3-8841-baa5cd490b58" />

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

Half adder:

module ex4(a,b,s,c);

input a,b;

output s,c;

xor g1(s,a,b);

and g2(c,a,b);

endmodule

Half subtractor:

module ex5(a,b,d,bout);

input a,b;

output d,bout;

assign d=a^b;

assign bout=(~a)&b;

endmodule


**RTL Schematic**

Half adder:
<img width="1920" height="1080" alt="Screenshot 2025-11-18 112627" src="https://github.com/user-attachments/assets/f6c586be-a1bb-46af-8944-4b0fe77670db" />

Half subtractor:
<img width="1920" height="1080" alt="Screenshot 2025-11-18 175221" src="https://github.com/user-attachments/assets/1185cf16-8ab9-4cac-a8cd-8df284acbba2" />




**Output/TIMING Waveform**

Half adder:
<img width="1920" height="1080" alt="Screenshot 2025-11-18 144045" src="https://github.com/user-attachments/assets/de9205e1-f37c-4187-b248-5478ed3ed752" />

Half subtractor:
<img width="1920" height="1080" alt="Screenshot 2025-11-18 180631" src="https://github.com/user-attachments/assets/553113fc-52d6-493f-aa6d-755c643f5d45" />

**Result:**
Hence Half adder and Half subtractor is successfully designed and verified using Verilog programming in the quartus software.
