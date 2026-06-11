# mean-and-varience-

AIM:

To Simulation Of Mean And Variance Using Scilab.
EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

THEORY:


Algorithm

1. Start the program.
2. Define the marginal probability density function.
3. Compute the mean values of X and Y using integration.
4. Compute E(X²) and E(Y²) using integration.
5. Calculate the variances of X and Y.
6. Display the mean and variance values.
7. Input two sequences from the user.
8. Compute the correlation between the sequences.
9. Plot the correlation sequence.
10. Stop the program.

Program
```
clear;
clc;
clear;

//Mean Value
function X=f(x),
z=3*(3-x)^2,//Marginal Probability Density Function
X=x*z
endfunction

a=0;
b=1;
EX=intg(a,b,f);//Mean value of X

function Y=c(y)
z=3*(3-y)^2,//Marginal Probability Density Function
Y=y*z
endfunction

EY=intg(a,b,c);//Mean value of Y

disp(EX,"i)Mean of X =")
disp(EY," Mean of Y =")

function X=g(x),
z=3*(3-x)^2,//Marginal Probability Density Function
X=x^2*z
endfunction

a=0;
b=1;
EX2=intg(a,b,g);

function Y=h(y)
z=3*(3-y)^2,//Marginal Probability Density Function
Y=y^2*z
endfunction

EY2=intg(a,b,h);

vX2=EX2-(EX)^2;//Variance of X
vY2=EY2-(EY)^2;//Variance of Y

disp(vX2,"ii)Variance of X");
disp(vY2," Variance of Y");

x= input("type in the reference sequence=");
y= input("type in the second sequence=");

n1=max(size(y))-1;
n2=max(size(x))-1;

r=corr(x,y,n1);

plot2d3('gnn',r);
```
MODEL GRAPH
 <img width="919" height="1290" alt="image" src="https://github.com/user-attachments/assets/55326c5b-7dd5-4873-aaf6-d219bb7c4420" />
 TABULATION:
<img width="637" height="332" alt="image" src="https://github.com/user-attachments/assets/7ff79056-9cf7-4ff0-a385-703060457972" />
Calculation
<img width="648" height="362" alt="image" src="https://github.com/user-attachments/assets/07db08ba-635e-410e-914a-efc758fa6b82" />

Output Waveform
<img width="760" height="580" alt="image" src="https://github.com/user-attachments/assets/3efbd926-dbb4-4692-9040-b72d6a7faf32" />

RESULT:
Thus the amplitude modulation and demodulation is experimentally done and the output is verified.
