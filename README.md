# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
NAME : BEATRICE THOMAS           REG NO: 23005036
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## HALF SUBTRACTOR:
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.

Diff= A^B
Borrow= A'B

## FULL SUBTRACTOR:
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 

Diff = A^B^C
Borrow = ~A &(B^C) |B & C

## Procedure
1. Create a New Project:
   - Open Quartus and create a new project by selecting "File" > "New Project Wizard."
   - Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2. Create a New Design File:
   - Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
   - Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3. Write the Combinational Logic Code:
   - Open the newly created Verilog or VHDL file and write the code for your combinational logic.
     
4. Compile the Project:
   - To compile the project, click on "Processing" > "Start Compilation" in the menu.
   - Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5. Analyze and Fix Errors:*
   - If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
   - Review and fix any issues in your code if necessary.
   - View the RTL diagram.

6.*Verification:
   - Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
   - Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
   - Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform.

## Program:
HALF SUBTRACTOR:  
module halfsub(a,b,difference,borrow);

input a,b;

output difference,borrow;

assign difference = a^b;

assign borrow = ~a&b;

endmodule 
<img width="439" alt="halfsub pro" src="https://github.com/23005036/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/140035214/dfd5b1ca-daf5-4d46-9322-ba514ff6c9dc">

FULL SUBTRACTOR :
module fs(output D, B, input X, Y, Z);

assign D = X^Y^Z;

assign B = ~X & (Y^Z) | Y & Z;

endmodule
<img width="361" alt="fullsub program" src="https://github.com/23005036/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/140035214/e73d2d92-7187-40e0-97b8-cb8ac24f164e">


## Output:
HALF SUB:  <img width="490" alt="HALFSUB OUTPUT" src="https://github.com/23005036/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/140035214/7e2eca96-b5a0-411d-8ded-a2c8e914b2e6">

FULL SUB: <img width="545" alt="fullsub output" src="https://github.com/23005036/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/140035214/4a98cac8-0b7e-4139-b0dc-a0650e8cfee4">


## Truthtable
HALF SUB:  ![HALF SUB (2)](https://github.com/23005036/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/140035214/035ffa2b-45f1-4867-bdde-ee9500771a2b)


FULL SUB: ![FULL SUB](https://github.com/23005036/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/140035214/21fb3642-16f9-49fb-a90d-c61fa2cf4dd3)

##  RTL realization
 HALF SUB:  <img width="362" alt="halfsub rtl" src="https://github.com/23005036/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/140035214/7e1650f7-7565-44aa-8e56-086bc4069715">

FULL SUB:  <img width="596" alt="fullsub rtl" src="https://github.com/23005036/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/140035214/61aa8674-b03f-4b57-9984-02c87414f971">


## Timing diagram 

HALF SUB:  <img width="431" alt="halfsub waveform" src="https://github.com/23005036/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/140035214/e8fdf95e-e2dd-4f14-afc2-23e665d0a166">

FULL SUB: <img width="743" alt="fullsub" src="https://github.com/23005036/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/140035214/8ae1d442-82a6-4f7f-b308-9dcd254da00a">


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
