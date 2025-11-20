# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB
## AIM
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## EQUIPMENTS NEEDED

•	Computer with i3 Processor
•	SCI LAB


## ALGORITHM
1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation
   
## PROCEDURE
•	Refer Algorithms and write code for the experiment.

•	Open SCILAB in System

•	Type your code in New Editor

•	Save the file

•	Execute the code

•	If any Error, correct it in code and execute again

•	Verify the generated results


## PROGRAM
  clc;
  clear;
  function fx = pdfx(x)
      z = 3*(1-x)^2;
      fx = x*z;
  endfunction
  a = 0;
  b = 1;
  EX = intg(a, b, pdfx);
  function fy = pdfy(x)
      z = 6*(1-x)^2;
      fy = x*z;
  endfunction
  EY = intg(a, b, pdfy);
  
  disp("1)Mean of X =",EX);
  disp("2)Mean of Y =",EY);
  
  function p = f1(u)
      q = 3*(1-u)^2;
      p = u^2 * q;
  endfunction
  
  a = 0;
  b = 1;
  
  EX2 = intg(a, b, f1);
  
  function r = f2(v)
      s = 6*(1-v)^2;
      r = v^2 * s;
  endfunction
  
  EY2 = intg(a, b, f2);
  
  vX2 = EX2 - (EX)^2;
  vY2 = EY2 - (EY)^2;
  
  disp("3) Variance of X =",vX2);
  disp("4)Variance of Y =",vY2);
  
  
  x= input("type in the reference sequence=");
  y= input("type in the second sequence=");
  S1=max(size(y))-1;
  S2=max(size(x))-1;
  r=corr(x,y,S1);
  plot2d3('gnn',r);
## CALCULATION
<img width="760" height="1280" alt="image" src="https://github.com/user-attachments/assets/8290983b-1c2b-4320-953f-8c7f7b755748" />
<img width="1044" height="744" alt="image" src="https://github.com/user-attachments/assets/64b2d246-2b8d-4cac-9106-a9366eeff0c7" />

## OUTPUT
<img width="563" height="351" alt="image" src="https://github.com/user-attachments/assets/cf95392e-63ab-4856-821f-53f16f7054ab" />
<img width="475" height="363" alt="image" src="https://github.com/user-attachments/assets/aeb7a44c-6384-473f-9e19-9745187928b8" />

## RESULT
Thus, the Mean,Variance and Cross-correlation are executed in scilab and output is verified.
