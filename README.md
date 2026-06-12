# mean-and-varience-

AIM:

To Simulation Of Mean And Variance Using Scilab.
EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

THEORY:

Mean and Variance are important statistical measures used to describe the characteristics of a random variable.

The Mean or Expected Value represents the average value of a random variable and indicates its central tendency. For a continuous random variable X with probability density function f(x), the mean is given by:

E(X) = ∫ x f(x) dx

Similarly, for a random variable Y,

E(Y) = ∫ y f(y) dy

Variance measures the spread or dispersion of the random variable about its mean. It indicates how far the values are distributed from the average value.

The variance of X is given by:

Var(X) = E(X²) – [E(X)]²

where,

E(X²) = ∫ x² f(x) dx

Similarly, the variance of Y is given by:

Var(Y) = E(Y²) – [E(Y)]²

where,

E(Y²) = ∫ y² f(y) dy

A small variance indicates that the values are clustered close to the mean, whereas a large variance indicates a wider spread of values.

Thus, the mean provides the average value of a random variable, while the variance provides a measure of its variability.



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

 TABULATION:
 <img width="732" height="886" alt="image" src="https://github.com/user-attachments/assets/6cd29964-5790-4c9b-9f1c-15bdd808fb2a" />

Calculation
<img width="335" height="465" alt="image" src="https://github.com/user-attachments/assets/a412b256-0884-4a8b-85c6-d72aaea25884" />
<img width="391" height="538" alt="image" src="https://github.com/user-attachments/assets/f970184c-828d-478c-90ff-72cbb3aee50b" />


Output Waveform
<img width="386" height="361" alt="image" src="https://github.com/user-attachments/assets/5eb6fae9-fb52-44a7-885e-2e236a6dca59" />

RESULT:
Thus, the mean and variance of the given random variables are determined using the specified probability density function and the results are verified.
