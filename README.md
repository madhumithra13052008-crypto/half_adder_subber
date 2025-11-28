# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

*AIM:*

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

*Equipments Required:*

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

*Half Adder*

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/user-attachments/assets/2b0c30fa-a085-4567-9cd5-f8809ac16bc4)


Figure -01 HALF ADDER

*Half Subtractor*

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

![image](https://github.com/user-attachments/assets/8372e670-4886-48bb-8369-820568a64d54)


Figure -02 HALF Subtractor

*Truthtable*
HALF ADDER

![image](https://github.com/user-attachments/assets/5ddc52ef-d125-4442-8265-139c2bb7c6e7)


HALF SUBTRACTOR

![image](https://github.com/user-attachments/assets/83ec047b-4a5b-42ea-ac00-af7c49740ea2)



*Procedure*

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


*Program:*


Program to design a half adder and half subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:Madhumithra.P
RegisterNumber:25013492


*Half Adder*

module half_adder (
    input  wire a, b,     // Inputs
    output wire sum,      // Sum output
    output wire carry     // Carry output
);

    // Logic equations
    assign sum   = a ^ b;   // XOR for sum
    assign carry = a & b;   // AND for carry

endmodule


*Half Subtractor*

module half_subtractor (
    input  wire a, b,         // Inputs
    output wire diff, borrow  // Outputs
);
    // Logic equations
    assign diff   = a ^ b;     // XOR for difference
    assign borrow = ~a & b;    // Borrow when a < b

endmodule

*RTL Schematic*
*Half Adder*
<img width="1920" height="832" alt="Screenshot (97)" src="https://github.com/user-attachments/assets/1e77b8e6-66f2-4207-8d19-1d948f4f029d" />

*Half Subtractor*
<img width="1920" height="799" alt="Screenshot (101)" src="https://github.com/user-attachments/assets/448c16d9-2fb0-4772-83b2-496c2fd5d22f" />

*Output/TIMING Waveform*
*Half Adder*
<img width="1920" height="900" alt="Screenshot (98)" src="https://github.com/user-attachments/assets/16f91c52-12e5-4d26-97d9-9e51d778fa71" />

*Half Subtractor*
<img width="1920" height="894" alt="Screenshot (102)" src="https://github.com/user-attachments/assets/390d092a-aaa2-445a-a523-719b709116d1" />

*Result:*

Thus the Half Adder and Half Subtractor are studied and the truth tables are verified
