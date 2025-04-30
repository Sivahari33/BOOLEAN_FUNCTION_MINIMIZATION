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

Developed by:K.SIVAHARIBALAN
RegisterNumber:24007220


module varun(a,b,c,d,w,x,y,z,f1,f2);
  input a,b,c,d,w,x,y,z;
  output f1,f2;
  wire x1,x2,x3,x4,x5,y1,y2,y3,y4,y5;
  assign x1=((~a)&(~b)&(~c)&(~d));
  assign x2=(a&(~c)&(~d));
  assign x3=((~b)&(c)&(~d));
  assign x4=((~a)&(b)&(c)&(d));
  assign x5=(b&(~c)&(d));
  assign f1=x1|x2|x3|x4|x5;
  
  assign y1=(x&(~y)&(z));
  assign y2=((~x)&(~y)&z);
  assign y3=((~w)&x&y);
  assign y4=(w&(~x)&(y));
  assign y5=(w&x&y);
  assign f2=y1|y2|y3|y4|y5;
  endmodule

**TRUTH TABLE**
![434138627-1af1a780-2863-41a7-8fba-1fd553c7618c](https://github.com/user-attachments/assets/8eccf293-97c9-4697-b207-e29a1870f7d0)

![434138642-66f485b5-8f60-4597-8b16-fdf98069a962](https://github.com/user-attachments/assets/849e093c-3747-4b15-9dba-5b85ca921825)



**RTL**

![434138727-fe7fc7c0-8d0a-428a-b5c3-a2a6dc6310aa](https://github.com/user-attachments/assets/a833321f-d2ba-42a9-a6a1-4f28facce70a)
![434138727-fe7fc7c0-8d0a-428a-b5c3-a2a6dc6310aa](https://github.com/user-attachments/assets/22fd95ce-577f-4fc0-b734-1206a644cee1)


**WAVEFORM**
![434138979-e3f247ea-7df4-4bdf-a025-a95f241e72fc](https://github.com/user-attachments/assets/8338a843-4955-4608-bb06-01a0e49cc9f4)



**Result:**
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

