# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
module experiment2(a, b, c, d, w, x, y, z, f1, f2);
input a, b, c, d, w, x, y, z;
output f1, f2;
wire x1, x2, x3, x4, x5, y1, y2, y3, y4, y5;
assign x1 = ((~a) & (~b) & (~c) & (~d));
assign x2 = (a & (~c) & (~d));
assign x3 = ((~b) & (c) & (~d));
assign x4 = ((~a) & b & c & d);
assign x5 = (b & (~c) & d);
assign f1 = x1 | x2 | x3 | x4 | x5;


assign y1 = (x & (~y) & z);
assign y2 = ((~x) & y & z);
assign y3 = ((~w) & x & y);
assign y4 = (w & (~x) & y);
assign y5 = (w & x & y);
assign f2 = y1 | y2 | y3 | y4 | y5;
endmodule
```


Developed by:DIVYASHREE B
RegisterNumber:212224040081


**RTL realization**

**Output:**

**RTL**

![Screenshot 2025-04-23 190723](https://github.com/user-attachments/assets/ab0a855f-f6f2-44f9-82f8-6ce605dace71)

**Timing Diagram**


![image](https://github.com/user-attachments/assets/eb11d821-c973-40e6-921f-e5661c40354e)


**Result:**
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

