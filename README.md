# VLSI-LAB-EXPERIMENTS
# AIM:
To simulate and synthesis Logic Gates,Adders and Subtractor using vivado 2023.2.

# APPARATUS REQUIRED:
vivado 2023.2

# PROCEDURE:
STEP:1 Start the vivado software, Select and Name the New project.

STEP:2 Select the device family, device, package and speed.

STEP:3 Select new source in the New Project and select Verilog Module as the Source type.

STEP:4 Type the File Name and module name and Click Next and then finish button. Type the code and save it.

STEP:5 Select the run simulation adn then run Behavioral Simulation in the Source Window and click the check syntax.

STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.

STEP:7 compare the output with truth table. Logic Diagram :
![image](https://github.com/Ocharan10/VLSI-LAB-EXP-1/assets/162343019/3ecf5062-4c6b-4dd1-85f2-4c809ae995c2)
# Logic Gates: 
# Half Adder:

![image](https://github.com/Ocharan10/VLSI-LAB-EXP-1/assets/162343019/e981f445-7473-402a-9e65-440072219863)
# Full adder:
![image](https://github.com/Ocharan10/VLSI-LAB-EXP-1/assets/162343019/3d462e09-9ef1-4d3e-9e09-dea943b2be2f)
# Half Subtractor:
![image](https://github.com/Ocharan10/VLSI-LAB-EXP-1/assets/162343019/a08561ad-54e7-48db-a7bc-39f602e84808)
# Full Subtractor:
![image](https://github.com/Ocharan10/VLSI-LAB-EXP-1/assets/162343019/2e419a8b-cd3e-42e3-b3f7-43e396ccea27)
# 8 Bit Ripple Carry Adder
![image](https://github.com/Ocharan10/VLSI-LAB-EXP-1/assets/162343019/555ca3fd-dfe0-4767-ac80-724254f0b065)

# VERILOG CODE:
LOGIC GATES: module logic(a,b,andgate,orgate,xorgate,nandgate,norgate,xnorgate,notgate );

input a,b;

output andgate,orgate,xorgate,nandgate,norgate,xnorgate,notgate;

and(andgate,a,b);

or(orgate,a,b);

xor(xorgate,a,b);

nand(nandgate,a,b);

nor(norgate,a,b);

xnor(xnorgate,a,b);

not(notgate,a);

endmodule

# HALF ADDER:
module HalfAdder(a,b,sum,carry);

input a,b;

output sum,carry;

xor (sum,a,b);

and (carry,a,b);

endmodule

# FULL ADDER:
module FA(a,b,cin,sum,cout);

input a,b,cin;

output sum,cout;

wire w1,w2,w3;

xor g1(w1,a,b);

and g2(w2,w1,cin);

and g3(w3,a,b);

xor g4(sum,w1,cin);

or g5(cout,w2,w3);

endmodule

# FULL SUBTRACTOR:
module full_sub(a,b,bin,diff,borrow);

input a,b,bin;

output diff,borrow;

wire w1,w2,w3;

xor g1(w1,a,bin);

and g2(w2,~a,b);

xor g3(diff,w1,bin);

or g4(borrow,w2,w3);

and g5(w3,~w1,bin);

endmodule

# HALF SUBTRACTOR:
module halfsubtractor(a,b,diff,borrow);

input a,b;

output diff,borrow;

xor g1(diff,a,b);

and g2(borrow,~a,b);

endmodule

# 8 BIT RIPPLE CARRY ADDER:
module fa(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

assign sum = a^b^c;

assign carry=(a&b)|(b&c)|(c&a);

endmodule

module rca(a,b,cin,sum,cout);

input [7:0]a,b; input cin;

output [7:0]sum;

output cout;

wire c1,c2,c3,c4,c5,c6,c7;

fa fa1(a[0],b[0],cin,sum[0],c1);

fa fa2(a[1],b[1],c1,sum[1],c2);

fa fa3(a[2],b[2],c2,sum[2],c3);

fa fa4(a[3],b[3],c3,sum[3],c4);

fa fa5(a[4],b[4],c4,sum[4],c5);

fa fa6(a[5],b[5],c5,sum[5],c6);

fa fa7(a[6],b[6],c6,sum[6],c7);

fa fa8(a[7],b[7],c7,sum[7],cout);

endmodule

# OUTPUT:
![image](https://github.com/Ocharan10/VLSI-LAB-EXP-1/assets/162343019/f4724cfb-14e1-4949-938b-bc76a5025c8c)


# HALF ADDER:
![image](https://github.com/Ocharan10/VLSI-LAB-EXP-1/assets/162343019/55d58fce-68f3-46ea-b151-51f5f59d03a4)


# FULL ADDER:
![image](https://github.com/Ocharan10/VLSI-LAB-EXP-1/assets/162343019/536c46fd-546a-4f96-8988-facee0d48691)


# HALF SUBTRACTOR:
 ![image](https://github.com/Ocharan10/VLSI-LAB-EXP-1/assets/162343019/eb63cb3b-bb45-47ff-a866-6aa9015f31b7)


# FULL SUBTRACTOR:
![image](https://github.com/Ocharan10/VLSI-LAB-EXP-1/assets/162343019/d2981316-bdbd-4e9f-ba08-d8fd2316727f)


# 8 BIT RIPPLE CARRY ADDER:
![image](https://github.com/Ocharan10/VLSI-LAB-EXP-1/assets/162343019/ad4cbd44-f52c-48d8-92fb-101600c7abd6)


# RESULT:
Thus the simulation and synthesis of Logic Gates,Adders and Subtractors using vivado has been sucessfully executed and verified .

