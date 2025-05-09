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
Full Adder
![432597863-adf18a0a-8e59-44bd-a08e-f899d0ab9b00](https://github.com/user-attachments/assets/bad96282-e9ec-4eed-9ae8-c4c123fc5885)
Full Subtractor
![432597992-a217361a-7151-461b-96f0-f86efe6a13a9](https://github.com/user-attachments/assets/c87e6a98-ffa6-4651-ae75-0d7da7e492c5)

**Procedure**

Write the detailed procedure here

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
EXP4A
```
module exp4a(sum, cout, a, b, cin);
    output sum;
    output cout;
    input a;
    input b;
    input cin;

	 wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=a&b;
	 assign w3=w1&cin;
	 assign sum=w1^cin;
	 assign cout=w2|w3;
endmodule
```
EXPB
```
module exp4b(df, bo, a, b, bin);
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
Developed by: KIRUPASAGAR RegisterNumber:212224230126

**RTL Schematic**
![431668697-78b5c73a-7e67-4a51-a26b-d3700837660a](https://github.com/user-attachments/assets/f45148a3-a767-419e-ae6d-5a5f2700a6e1)
![431694170-7cf94ec3-79e6-4734-b3bd-055ebacb6b90](https://github.com/user-attachments/assets/ec989d34-d40b-4673-8af8-f1c6d4fd4b19)

**Output Timing Waveform**
![431668836-b802f998-2f45-4702-b529-7aea82a985cd](https://github.com/user-attachments/assets/ff904916-376e-4d87-868b-9430a1ed3ca7)
![Uploading 431694396-970cf525-a319-4fe6-9f07-95aef67bc5b5.png…]()

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



