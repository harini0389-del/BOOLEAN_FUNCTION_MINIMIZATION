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

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by:Harini M RegisterNumber:*/212225240047
```
module boolean(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
and(s,ydash,z);
and(t,x,y);
and(u,w,y);
or(f2,s,t,u);
endmodule
```
**RTL realization**
<img width="1907" height="569" alt="image" src="https://github.com/user-attachments/assets/c7cee0e0-40e0-42ad-a6b0-076c26f0f765" />
**Output:**

**RTL**
<img width="1912" height="790" alt="image" src="https://github.com/user-attachments/assets/a6391527-d165-4618-b46e-c80482aa9351" />

**Timing Diagram**
<img width="1745" height="999" alt="image" src="https://github.com/user-attachments/assets/032e3419-d185-468e-9c7b-dd2cd0c40538" />

**Result:**
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

