### name: S.NADISH
### REG NO:212224050023
### DATE: 08/04/2025 


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
![435719912-090eb3a5-8cfe-47ff-93c2-bc1db8e0800e](https://github.com/user-attachments/assets/c8c22424-924a-4101-b1e2-d077b4db2a1d)
**Procedure**
Write the detailed procedure here
**Program:**
module ex4(sum, cout, a, b, cin);
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

module ex44(df, bo, a, b, bin);
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
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
**RTL Schematic**
![435720402-9d085187-9b9d-4769-9f30-26551a98024b](https://github.com/user-attachments/assets/4849f13f-af92-4f6b-a744-0ceef775bd81)
![435720524-948c3e11-4870-46a6-b921-3e6776370d2b](https://github.com/user-attachments/assets/541951b3-2635-4970-ad17-eeea54e98655)
**Output Timing Waveform**
![435720602-c27a3047-7ca1-42ca-b48a-11d67b584abd](https://github.com/user-attachments/assets/1037e791-3dd2-4567-b834-76b5bd688279)
![435720670-8f77d0a2-8e12-4b94-8f81-66322b53e1de](https://github.com/user-attachments/assets/5eb0aafb-337f-421b-bf42-8dbcfe40d7bb)
**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



